<!-- SearchBarComponent.vue -->

<template>
    <div>
        <div class="search__bar">
            <input type="text" placeholder="Search..." class="search__bar-input" />
            <button  class="search__bar-button">Search</button>
        </div>
    </div>
  </template>
  
  
  <style scoped>
  .search__bar {
    display: flex;
    width: 400px ; 
    align-items: center;
    margin: 2vh 0; 
  }
  
  .search__bar-input {
    flex: 1;
    padding: 10px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
    margin-right: 10px;
  }
  
  .search__bar-button {
    background-color: #3498db;
    color: #fff;
    padding: 10px 15px;
    font-size: 16px;
    border: none;
    cursor: pointer;
    border-radius: 4px;
    transition: background-color 0.3s ease;
  }
  
  .search__bar-button:hover {
    background-color: #2980b9;
  }
  </style>
  