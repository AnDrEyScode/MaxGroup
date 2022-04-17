<template>
  <div class="serve-galery-container">

    <div class="serve-btns">
      <input type="image" :src="require('@/assets/icons/arrowLeft.png')" alt="ArrowLeft" @click="galeryMoveLeft">
      <input type="image" :src="require('@/assets/icons/arrowRight.png')" alt="ArrowRight" @click="galeryMoveRight">
    </div>

    <div class="serve-galery">
      <h2>Наши услуги</h2>
      <div class="galery-wnd"><serve-galery class="galery" :scroll="scroll" :serveItems="serveItems" /></div> 
    </div>

  </div>
  
</template>

<script>
import ServeGalery from '@/components/ServeGalery.vue'
import axios from 'axios'


export default {
  components: { ServeGalery },
  data(){
    return {
      serveItems: [],
      scroll: 0
    }
  },

  methods: {
    galeryMoveLeft(){
      if (this.scroll < 0)
        this.scroll += 430
    },

    galeryMoveRight(){
      if (document.querySelector('.galery').offsetWidth + this.scroll > document.querySelector('.galery-wnd').offsetWidth)
        this.scroll -= 430
    }
  },

  mounted(){
     fetch('data/serveItems.json')
     .then(response => response.json())
     .then(json => this.serveItems = json.serveItems)
     .catch(e => console.log(e))
  }
}
</script>

<style scoped>
  .serve-galery-container{
    height: 70vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .serve-btns{
    align-self: flex-end;
    margin: 20px 60px;
  }

  .serve-btns > input:first-child{
    margin-right: 20px;
  }

  .serve-galery{
    height: 80%;
    display: flex;
    align-items: center;
  }

  .serve-galery > h2{
    width: 500px;
    margin-left: 50px;
    color: #2C2450;
  }

  .galery-wnd{
    height: 100%;
    width: 100%;
    position: relative;
    overflow: hidden;
  }
</style>