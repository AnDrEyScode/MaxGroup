<template>
  <header class="header">
    <input type="image" :src="require('@/assets/icons/menuBtn.png')" alt="menuBtn" class="menu-button" @click="toggleMenu">
    <div class="header-container">
      <div class="logo">
        <img src="@/assets/logo.png" alt="logo">
      </div>
      <nav class="navbar">
        <ul class="menu">
          <li class="menu-item">Наши проекты</li>
          <li class="menu-item">Контакты</li>
          <li class="menu-item">О нас</li>
          <li class="menu-item">Услуги</li>
        </ul>
      </nav>
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
  }

  .logo:hover{
    cursor: pointer;
  }

  /* @media screen and (max-width: 600px) {
    .header{
      position:static;
    }
    .header-container{
      margin: 10px 0px;
    }

    .navbar{
      z-index: 1000;
      background: #fff;
      order: -1;
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