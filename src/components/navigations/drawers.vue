<template>
    <div>
      <div v-for="(drawer, index) in drawers" :key="index" class="drawer-container">
        <button @click="toggleDrawer(index)" class="drawer-button">{{ drawer.title }}</button>
        <transition :name="transitionName">
          <div v-if="drawer.open" class="drawer-content">
            <div @click="closeDrawer(index)" class="overlay"></div>
            <div class="drawer-inner">
              <div class="drawer-header">
                <span>{{ drawer.title }}</span>
                <button @click="closeDrawer(index)" class="close-button">X</button>
              </div>
              <div class="drawer-body">
                <slot :drawerIndex="index"></slot>
              </div>
            </div>
          </div>
        </transition>
      </div>
    </div>
  </template>
  
  <script>
export default { 
  props: ['drawers'] , 
  data() {
    return {
      drawers: this.drawers,
      transitionName: 'fade',
    };
  },
  methods: {
    toggleDrawer(index) {
      const drawer = this.drawers[index] || {};
      this.$set(this.drawers, index, { title: drawer.title, open: !drawer.open });
    },
    closeDrawer(index) {
      const drawer = this.drawers[index] || {};
      this.$set(this.drawers, index, { title: drawer.title, open: false });
    },
  },
};
  </script>
  
  <style scoped>
  .drawer-container {
    position: relative;
    margin-bottom: 10px;
  }
  
  .drawer-button {
    cursor: pointer;
    padding: 8px;
  }
  
  .drawer-content {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 1;
  }
  
  .drawer-inner {
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    z-index: 2;
    width: 300px; /* Adjust the width as needed */
  }
  
  .drawer-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
  }
  
  .close-button {
    cursor: pointer;
    background: none;
    border: none;
    font-size: 16px;
    color: #333;
  }
  </style>
  