<template>
  <div class="preferences">
    <div class="preferences-container">

      <div class="preference-item">
        <input type="image" :src="require('@/assets/icons/prefer1.png')" alt="prefer1">
        <p>30 выполненных проектов</p>
      </div>

      <div class="preference-item">
        <input type="image" :src="require('@/assets/icons/prefer2.png')" alt="prefer2">
        <p>высококвалифицированные рабочие</p>
      </div>

      <div class="preference-item">
        <input type="image" :src="require('@/assets/icons/prefer3.png')" alt="prefer3">
        <p>современное оборудование</p>
      </div>

      <div class="preference-item">
        <input type="image" :src="require('@/assets/icons/prefer4.png')" alt="prefer4">
        <p>индивидуальный подход</p>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  .preferences{
    height: 30vh;
    width: 100%;
    background: #2C2450;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #fff;
  }

  .preferences-container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }

  .preference-item{
    margin: 0px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: max-content;
  }

  .preference-item > p{
    text-align: center;
    font-size: 14px;
    line-height: 17px;
    margin: 15px 0px;
    width: 200px;
  }

  .preference-item > input{
    width: 90px;
    height: auto;
  }
</style>