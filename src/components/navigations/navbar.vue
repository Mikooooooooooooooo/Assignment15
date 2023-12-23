<template>
    <div>
        <div class="navbar">
            <div class="navbar-header">
                <h2 class="navbar-title">{{ title }}</h2>
            </div>
            <nav class="navbar-nav">
                <ul class="navbar-list">
                <li class="navbar-option" v-for="menuItem in menuItems" :key="menuItem.id">
                    <a class="navbar-link" :href="menuItem.route">{{ menuItem.text }}</a>
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
   .navbar{
    width: 250px;
    background-color: #34495e;
    color: #ecf0f1;
    padding: 20px;
    box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
  }
  
  .navbar-header {
    margin-bottom: 20px;
  }
  
  .navbar-title {
    margin: 0;
    font-size: 20px;
  }
  
  .navbar-list {
    list-style-type: none;
    padding: 0;
  }
  
  .navbar-option{
    margin-bottom: 10px;
  }
  
  .navbar-link {
    color: #ecf0f1;
    text-decoration: none;
    font-size: 16px;
    display: block;
    transition: color 0.3s ease;
  }
  
  .navbar-link:hover {
    color: #3498db;
  }
  </style>