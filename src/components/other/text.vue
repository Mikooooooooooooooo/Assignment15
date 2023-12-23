<template>
    <div>
      <p v-if="variant === 'body'">{{ text }}</p>
      <h1 v-else-if="variant === 'heading1'">{{ text }}</h1>
      <h2 v-else-if="variant === 'heading2'">{{ text }}</h2>
      <h3 v-else-if="variant === 'heading3'">{{ text }}</h3>
      <h4 v-else-if="variant === 'heading4'">{{ text }}</h4>
      <h5 v-else-if="variant === 'heading5'">{{ text }}</h5>
      <h6 v-else-if="variant === 'heading6'">{{ text }}</h6>
      <span v-else>{{ text }}</span>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      text: {
        type: String,
        required: true,
      },
      variant: {
        type: String,
        default: 'body',
        validator: (value) => ['body', 'heading1', 'heading2', 'heading3', 'heading4', 'heading5', 'heading6'].includes(value),
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add styles for different text variants as needed */
  body {
    font-family: 'Arial', sans-serif;
  }
  
  p {
    font-size: 16px;
    line-height: 1.5;
  }
  
  h1 {
    font-size: 32px;
    line-height: 1.2;
  }
  
  h2 {
    font-size: 28px;
    line-height: 1.3;
  }
  
  h3 {
    font-size: 24px;
    line-height: 1.4;
  }
  
  h4 {
    font-size: 20px;
    line-height: 1.5;
  }
  
  h5 {
    font-size: 18px;
    line-height: 1.6;
  }
  
  h6 {
    font-size: 16px;
    line-height: 1.7;
  }
  </style>