<template>
    <div>
        <header class="page__header">
        <div class="container">
            <h1 class="page__title">{{ title }}</h1>
            <nav class="page__nav">
                <ul class="page__list">
                <li class="page__option" v-for="link in links" :key="link.id">
                    <a class="page__link" :href="link.url">{{ link.text }}</a>
                </li>
                </ul>
            </nav>
        </div>
        </header>
    </div>
  </template>
  
<script>
  export default {
    props: {
      title: String,
      links: Array,
    },
  };
</script>
  
<style scoped>
 .page__header {
  background-color: #2c3e50;
  color: #ecf0f1;
  padding: 15px 0;
  width: 600px ;
}

.container {
  width: 80%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.page__title {
  margin: 0;
  font-size: 24px;
}

.page__nav {
  margin-top: 10px;
}

.page__list {
  list-style-type: none;
  padding: 0;
  display: flex;
}

.page__option {
  margin-right: 20px;
}

.page__link {
  color: #ecf0f1;
  text-decoration: none;
  font-weight: bold;
  font-size: 16px;
  transition: color 0.3s ease;
}

.page__link:hover {
  color: #3498db;
}
  </style>