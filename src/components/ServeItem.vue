<template>
  <div class="serve-item">
    <img :src="serveItem.path" alt="">
    <div class="serve-item-content">
      
      <h3>{{ serveItem.title }}</h3>
      <p>{{ serveItem.body }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    serveItem: {
      type: Object,
      required: true
    }
  },

  data(){
    return { imgSrc: ''}
  },


}
</script>

<style scoped>
  .serve-item{
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    width: 400px;
    height: 100%;
    
    position: relative;
    /* border: 2px solid black; */
    margin: 0px 15px;
    overflow: hidden;
    color: #fff;
  }

  .serve-item-content{
    height: 30%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    background: rgba(17, 6, 68, 0.3);
    backdrop-filter: blur(3px);
    padding: 20px;
  }

  .serve-item img{
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;

  }
</style>