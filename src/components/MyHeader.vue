<template>
  <header class="header">
    <div class="menu-button">
      <input type="image" :src="require('@/assets/icons/menuBtn.png')" alt="menuBtn" @click="toggleMenu">
    </div>
    <div class="header-container">
      <!-- <div class="menu-place"></div> -->
      <div class="logo">
        <img src="@/assets/logo.png" alt="logo">
      </div>
      <!-- <input type="image" :src="require('@/assets/icons/menuBtn.png')" alt="menuBtn" class="menu-button" @click="toggleMenu"> -->
      <div class="nav">
        <nav class="navbar">
          <ul class="menu">
            <li class="menu-item">Наши проекты</li>
            <li class="menu-item">Контакты</li>
            <li class="menu-item">О нас</li>
            <li class="menu-item">Услуги</li>
          </ul>
        </nav>
      </div>
      
      <div class="phone">
        +7 (945) 647 24-38
      </div>
    </div>
  </header>
  
  
</template>

<script>
export default {
  methods: {
    toggleMenu(){
      document.querySelector('.navbar').classList.toggle('visible')
    }
  }
}
</script>

<style scoped>
  .header{
    position: fixed;
    background-color: #fff;
    width: 100%;
    z-index: 1000;
    color: #2C2450;
    /* display: flex;
    justify-content: flex-end; */
  }

  .header-container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 10px 75px;
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 22px;
  }

  .nav{
    position: relative;
  }

  .menu{
    display: flex;
    justify-content: space-around;
  }

  .menu-item{
    list-style: none;
    margin: 0px 15px;
  }

  .menu-item:hover{
    text-decoration: underline;
    cursor: pointer;
  }

  .menu-button{
    display: none;
    position: absolute;
    height: 40px;
    width: 40px;

  }
  
  .menu-button > input{
    margin: auto;
  }

  .logo:hover{
    cursor: pointer;
  }

  @media screen and (max-width: 800px) {
    .header{
      position:static;
    }

    .header-container{
      margin: 10px 0px;
    }

    .header-container > *{
      display: flex;
      align-items: center;
    }

    .nav{
      order: -1;
      flex: 0 0 100px;
    }

    .navbar{
      z-index: 1001;
      background: #fff;
      position: fixed;
      left: 0px;
      top: 0px;
      visibility: hidden;
    }

    .menu{
      padding: 40px 10px;
      flex-direction: column;
      background: #fff;
      
    }

    .menu-item{
      list-style: none;
      margin: 15px 0px;
      text-decoration: underline;
      width: 100%;
      border-bottom:1px solid #C2C2C2;
      text-decoration: none;
    }


    .menu-button{
      display: block;
      position: fixed;
      left: 0;
      top: 0;
      z-index: 1000;
      padding: 12.5px 10px;
      background: #fff;
      border-radius: 0px 20px 20px 0px;
    }

    

    .visible{
      visibility: visible;
    }

    .logo > img{
      height: 40px;
      width: auto;
    }

    
  }

  @media screen and (max-width: 480px){
    .logo > img{
      height: 20px;
      width: auto;
    }

    .phone{
      font-style: normal;
      font-weight: 600;
      font-size: 7px;
      line-height: 9px;
      margin-right: 20px;
    }

    .menu-button > input{
      /* width: 20px; */
      height: 15px;
    }


  }


  /* @media screen and (max-width: 600px) {
    .header{
      position:static;
    }

    .header-container{
      margin: 10px 0px;
      flex: 1 1 auto;
    }

    .navbar{
      z-index: 1000;
      background: #fff;
      position: fixed;
      left: 0px;
      top: 0px;
      visibility: hidden;
    }


    .menu{
      padding: 40px;
      flex-direction: column;
      background: rgba(17, 6, 68, 0.3);
    }

    .menu-item{
      list-style: none;
      margin: 15px 0px;
      text-decoration: underline;
    }

    .menu-button{
      display: block;
      position: fixed;
      left: 20px;
      top: 20px;
      z-index: 1001;
    }

    .menu-place{
      display:block;
      margin: 0px 20px;
    }

    .visible{
      visibility: visible;
    }

    .logo{
      justify-self: center;
    }

    .phone{
      justify-self: right;
    }
    
  } */
</style>