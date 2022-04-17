<template>
  <div class="galery">
    <serve-item v-for="item in serveItems" :key="item.id" :serveItem="item"/>
  </div>
</template>

<script>
import ServeItem from '@/components/ServeItem.vue'
export default {
  components: { ServeItem },
  props: {
    serveItems: {
      type: Array,
      required: true
    },

    scroll: {
      type: Number,
      required: true
    }
  },

  watch: {
    scroll(newValue){
      document.querySelector('.galery').style.left = newValue + 'px'
    }
  },

}
</script>

<style scoped>
  .galery{
    display: flex;
    flex: 0 0 auto;
    position: absolute;
    height: 100%;
    width: max-content;
    transition: left 1s ease;
    left: 0px;
  }
</style>