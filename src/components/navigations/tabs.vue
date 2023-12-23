<template>
    <div>
        <div class="tabs">
            <div class="tab-header">
                <div v-for="(tab, index) in tabs" :key="index" @click="changeTab(index)" :class="{ 'active': activeTab === index }" class="tab-item">
                {{ tab.title }}
                </div>
            </div>
            <div class="tab-content">
                <slot :tabIndex="activeTab"></slot>
            </div>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeTab: 0,
      };
    },
    props: {
      tabs: {
        type: Array,
        required: true,
      },
    },
    methods: {
      changeTab(index) {
        this.activeTab = index;
      },
    },
  };
  </script>
  
  <style scoped>

  .tabs{
    width: 400px ; 
  }
  .tab-header {
    display: flex;
  }
  
  .tab-item {
    cursor: pointer;
    padding: 10px;
    margin-right: 10px;
    border: 1px solid #ccc;
    border-bottom: none;
    border-radius: 5px 5px 0 0;
  }
  
  .tab-item.active {
    background-color: #3498db;
    color: #fff;
  }
  
  .tab-content {
    border: 1px solid #ccc;
    padding: 10px;
    border-radius: 0 0 5px 5px;
  }
  </style>
  