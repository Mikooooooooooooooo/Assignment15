<template>
    <div class="list__group">
      <div v-for="(item, index) in items" :key="index" class="list__group-item">
        {{ item }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      items: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .list__group {
    width: 400px ; 
    display: flex;
    flex-direction: column;
    padding: 10px;
  }
  
  .list__group-item {
    background-color: #fff;
    border: 1px solid #ddd;
    padding: 10px;
    margin-bottom: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .list__group-item:hover {
    background-color: #f5f5f5;
  }
  </style>