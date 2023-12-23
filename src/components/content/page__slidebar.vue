<template>
    <div>
        <div class="page__slidebar">
            <div class="page__sidebar-header">
                <h2 class="page__slidebar-title">{{ title }}</h2>
            </div>
            <nav class="page__slidebar-nav">
                <ul class="page__slidebar-list">
                <li class="page__slidebar-option" v-for="menuItem in menuItems" :key="menuItem.id">
                    <a class="page__slidebar-link" :href="menuItem.route">{{ menuItem.text }}</a>
                </li>
                </ul>
            </nav>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      menuItems: Array,
    },
  };
  </script>
  
  <style scoped>
  /* Add your styles here */
   .page__slidebar{
    width: 250px;
    background-color: #34495e;
    color: #ecf0f1;
    padding: 20px;
    box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
  }
  
  .page__sidebar-header {
    margin-bottom: 20px;
  }
  
  .page__slidebar-title {
    margin: 0;
    font-size: 20px;
  }
  
  .page__slidebar-list {
    list-style-type: none;
    padding: 0;
  }
  
  .page__slidebar-option{
    margin-bottom: 10px;
  }
  
  .page__slidebar-link {
    color: #ecf0f1;
    text-decoration: none;
    font-size: 16px;
    display: block;
    transition: color 0.3s ease;
  }
  
  .page__slidebar-link:hover {
    color: #3498db;
  }
  </style>