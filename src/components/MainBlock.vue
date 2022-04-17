<template>
  <div class="main">
    <div class="main-content">
      <h1>Заголовок на одну строку</h1>
      <p>
        Компания «Макс Групп» — это собственное производство уличной мебели и малых архитектурных форм (МАФ), помощь в разработке проектов по благоустройству городских и частных территорий. 
      </p>
      <my-button class="blue" value="Посмотреть работы"/>
    </div>
  </div>
</template>

<script>
export default {

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

  .main-content > p{
    width: 700px;
    text-align: center;
    font-weight: 400;
    font-size: 18px;
    line-height: 22px;
  }
</style>