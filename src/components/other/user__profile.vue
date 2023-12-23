<template>
    <div class="user-profile">
      <img :src="user.image" :alt="user.name" class="profile-image" />
      <div class="user-info">
        <h3>{{ user.name }}</h3>
        <p>{{ user.email }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      user: {
        type: Object,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .user-profile {
    display: flex;
    align-items: center;
  }
  
  .profile-image {
    border-radius: 50%;
    width: 80px;
    height: 80px;
    margin-right: 20px;
  }
  
  .user-info {
    display: flex;
    flex-direction: column;
  }
  
  h3 {
    margin: 0;
  }
  
  p {
    margin: 5px 0;
    color: #888;
  }
  </style>