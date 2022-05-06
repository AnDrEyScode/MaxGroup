<template>
  <div class="main">
    <div class="main-content">
      <h1>Заголовок на одну строку</h1>
      <p>
        Компания «Макс Групп» — это собственное производство уличной мебели и малых архитектурных форм (МАФ), помощь в разработке проектов по благоустройству городских и частных территорий. 
      </p>
      <my-button class="blue main-btn" value="Посмотреть работы" @click="moveToProjects"/>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    moveToProjects(){
      location.href = '#projects'
    }
  }
}
</script>

<style scoped>
  .main{
    height: 100vh;
    background-image: url("@/assets/background/main.png");
    background-repeat: no-repeat;
    background-size:cover;
    display: flex;
    align-items: center;
  }

  .main-content{
    position: relative;
    width: 1000px;
    height: 30%;
    margin: auto;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    color: #fff;
  }

  .main-content > h1{
    text-align: center;
    font-style: normal;
  }

  .main-content > p{
    width: 700px;
    font-style: normal;
    text-align: center;
    font-weight: 400;
    font-size: 18px;
    line-height: 22px;
  }

  .main-btn{
    width: 300px;
  }

  @media screen and (max-width: 800px) {
    .main-content{
      width: 70%;
    }

    .main-content > h1{
      font-weight: 600;
      font-size: 40px;
      line-height: 49px;
      width: 100%;
    }


    .main-content > p{
      font-weight: 400;
      font-size: 16px;
      line-height: 20px;
      width: 100%;
    }

    .main-btn{
      width: 230px;
    }
  }

  @media screen and (max-width: 600px) {
    .main-content{
      width: 90%;
    }

    .main-content > h1{
      font-weight: 600;
      font-size: 20px;
      line-height: 24px;
      width: 100%;
    }


    .main-content > p{
      font-weight: 400;
      font-size: 10px;
      line-height: 12px;
      width: 100%;
    }

    .main-btn{
      width: 100%;
    }
  }
</style>