<template>
  <my-header></my-header>
  <router-view to="/"/>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
export default {
components: {
  MyHeader
}
}
</script>

<style>
@font-face {
    font-family: "Montserrat";
    src: url("@/fonts/Montserrat/Montserrat-VariableFont_wght.ttf");
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
  font-family: "Montserrat";
}


h1 {
  font-size: 64px;
  line-height: 78px;
}

h2 {
  font-size: 36px;
  line-height: 44px;
}



</style>
