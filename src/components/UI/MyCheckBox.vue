<template>
  <div class="check-box-container"><input class="check-box" type="checkbox" name="a" id=""><label><slot></slot></label></div>
  
</template>

<script>
export default {
  name: "my-check-box",
}
</script>

<style scoped>
  .check-box-container{
    color: #fff;
    font-style: normal;
    font-weight: 300;
    font-size: 10px;
    line-height: 12px;
  }

  .check-box:not(:checked){
    background-color: #2C2450;
    border: 1px solid #fff;
    margin-right: 5px;
  }

  .check-box:checked{
    background-image: url('@/assets/icons/checked.png');
  }
</style>