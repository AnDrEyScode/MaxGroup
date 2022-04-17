<template>
  <footer class="footer">


    <div class="footer-container">
      <div class="socials">
        <input type="image" :src="require('@/assets/icons/fb.png')" alt="facebook">
        <input type="image" :src="require('@/assets/icons/vk.png')" alt="vk">
      </div>

      <img src="@/assets/logoWhite.png" alt="logo" class="logo">

      <div class="phone">
        +7 (945) 647 24-38
      </div>
    </div>

    
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
  .footer{
    background-color: #2C2450;
    width: 100%;
    padding: 15px 75px;
  }

  .footer-container{
    margin: auto;

    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .socials{
    display: flex;
    align-items: center;
  }

  .socials > input {
    width: 30px;
    height: auto;
    margin-right: 5px;
  }

  .phone{
    color: #fff;
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
  }
</style>