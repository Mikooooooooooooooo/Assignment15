
 <template>
    <div class="progress-bar" :style="{height: height + 'px'}">
      <div class="progress" :style="{ width: percent + '%' }"></div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      percent: {
        type: Number,
        required: true,
        validator: value => value >= 0 && value <= 100
      } , 
      height: { 
        type: Number , 
        required: true , 
        validator: value => value >= 0 
      }
    }
  };
  </script>
  
  <style scoped>
  .progress-bar {
    width: 400px ; 
    height: 20px;
    background-color: #e0e0e0;
    border-radius: 4px;
    overflow: hidden;
  }
  
  .progress {
    height: 100%;
    background-color: #4caf50;
    transition: width 0.3s ease;
  }
  </style>