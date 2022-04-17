<template>
  <input class="my-input" :type="inputType">
</template>

<script>
export default {
  name: 'my-input',
  props: {
    
    inputType: {
      type: String,
      default: 'text',
    }
  }
}
</script>

<style scoped>
  .my-input{
    padding: 20px 15px;
    border: 2px solid #fff;
    background: #2C2450;
    color: #fff;
  }

  
</style>