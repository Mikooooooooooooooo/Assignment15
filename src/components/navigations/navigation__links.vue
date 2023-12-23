<template>
    <nav class="navigation__links">
      <ul class="navigation__links-list">
        <li v-for="(link, index) in links" :key="index" class="navigation__links-item">
          <a :href="link.to" class="navigation__links-link" active-class="active">{{ link.text }}</a>
        </li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    props: {
      links: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .navigation__links-list {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
  }
  
  .navigation__links-item {
    margin-right: 10px;
  }
  
  .navigation__links-link {
    text-decoration: none;
    color: #333;
    padding: 8px;
    border-radius: 4px;
    transition: background-color 0.3s;
  }
  
  .navigation__links-link:hover {
    background-color: #f5f5f5;
    cursor: pointer ; 
  }
  
  .nav-link.active {
    background-color: #3498db;
    color: #fff;
  }
  </style>