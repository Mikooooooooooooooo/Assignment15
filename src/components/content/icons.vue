<template>
  <div>
      <img :src="source" alt="" class="image">
  </div>
</template>

<script>
  export default{ 
      props: ['source']
  }
</script>

<style>
  .image{ 
      width: 500px ; 
  }
</style>