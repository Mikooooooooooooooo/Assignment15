<!-- BreadcrumbComponent.vue -->

<template>
    <nav class="breadcrumb">
      <ul class="breadcrumb__list">
        <li class="breadcrumb__option" v-for="(item, index) in items" :key="index">
          <a class="breadcrumb__link" :href="item.route">{{ item.text }} </a>
          <span class="breadcrumb__slash">/</span>
        </li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    props: {
      items: Array,
    },
  };
  </script>
  
  <style scoped>
  .breadcrumb {
    font-size: 16px;
    margin-bottom: 20px;
  }
  
  .breadcrumb__list {
    list-style-type: none;
    padding: 0;
    display: flex;
  }
  
  .breadcrumb__option {
    margin-right: 5px;
  }
  
  .breadcrumb__link {
    color: #3498db;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  
  .breadcrumb__link:hover {
    color: #2980b9;
  }
  
  .breadcrumb__option:last-child:last-child {
    font-weight: bold;
    color: #555;
  }


  </style>
  