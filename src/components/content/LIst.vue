<template>
    <div class="list">
      <h2 class="list__title">{{ title }}</h2>
      <ul class="list__list">
        <li class="list__option" v-for="item in items" :key="item.id">{{ item.text }}</li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      items: Array,
    },
  };
  </script>
  
  <style scoped>
    .list {
      width: 400px ;
      border: 1px solid #ddd;
      padding: 10px;
      margin: 10px 0;
    }
  
    .list__title {
      color: #333;
      font-size: 18px;
      margin-bottom: 10px;
    }
  
    .list__list {
      list-style-type: none;
      padding: 0;
    }
  
    .list__option {
      margin-bottom: 5px;
      padding: 5px;
      background-color: #f4f4f4;
      border-radius: 4px;
    }
  </style>