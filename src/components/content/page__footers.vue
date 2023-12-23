
<template>
    <div>
        <footer class="page__footers">
            <div class="container">
                <p class="page__footers-year">&copy; {{ currentYear }} My App</p>
                <nav class="page__footers-nav">
                <ul class="page__footers-list">
                    <li class="page__footers-option" v-for="link in links" :key="link.id">
                    <a :href="link.url" class="page__footers-link">{{ link.text }}</a>
                    </li>
                </ul>
                </nav>
            </div>
        </footer>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      links: Array,
    },
    data() {
      return {
        currentYear: new Date().getFullYear(),
      };
    },
  };
  </script>
  
  <style scoped>
  .page__footers {
    background-color: #2c3e50;
    color: #ecf0f1;
    padding: 15px 0;
    margin-top: 20px;
    width: 600px ; 
  }
  
  .container {
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .page__footers-year {
    margin: 0;
    font-size: 14px;
  }
  
  .page__footers-nav {
    margin-top: 10px;
  }
  
  .page__footers-list {
    list-style-type: none;
    padding: 0;
    display: flex;
  }
  
  .page__footers-option {
    margin-right: 20px;
  }
  
  .page__footers-link {
    color: #ecf0f1;
    text-decoration: none;
    font-weight: bold;
    font-size: 14px;
    transition: color 0.3s ease;
  }
  
  .page__footers-link:hover {
    color: #3498db;
  }
  </style>
  