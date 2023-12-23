<template>
    <div>
        <div class="tag">
            <slot></slot>
        </div>
    </div>
  </template>
  
  <style scoped>
  .tag {
    display: inline-block;
    padding: 0.5em 1em;
    margin: 0.2em;
    border-radius: 5px;
    background-color: #e0e0e0;
    color: #333;
    font-size: 14px;
    cursor: default;
  }
  
  </style>