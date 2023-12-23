<template>
    <div>
      <div v-for="(group, index) in linkGroups" :key="index" class="link-group">
        <h2 class="group-title">{{ group.title }}</h2>
        <ul class="link-list">
          <li v-for="(link, linkIndex) in group.links" :key="linkIndex" class="link-item">
            <a :href="link.href" class="nav-link" :target="link.target || '_self'">{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      linkGroups: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .link-group {
    margin-bottom: 20px;
  }
  
  .group-title {
    font-size: 18px;
    margin-bottom: 10px;
  }
  
  .link-list {
    list-style-type: none;
    padding: 0;
    margin: 0;
  }
  
  .link-item {
    margin-bottom: 5px;
  }
  
  .nav-link {
    text-decoration: none;
    color: #333;
    padding: 8px;
    border-radius: 4px;
    transition: background-color 0.3s;
    display: inline-block;
  }
  
  .nav-link:hover {
    background-color: #f5f5f5;
  }
  
  </style>
  