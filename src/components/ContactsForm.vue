<template>
  <div class="contacts-form">
    <h2>Свяжитесь с нами!</h2>
    <form class="form" action="">
      <div class="form-inputs">
        <my-input class="form-input" placeholder="Имя"/> <my-input class="form-input" :inputType="'phone'" placeholder="Телефон"/> <my-button class="form-input white" :value="'Отправить'"/>
      </div>
      <my-check-box>Я даю согласие на <a style="text-decoration: underline;">обработку персональных данных</a> и соглашаетесь с политикой конфиденциальности</my-check-box>
      <!-- <input type="checkbox" value="Я даю согласие на обработку персональных данных и соглашаетесь с политикой конфиденциальности"> -->
      
    </form>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  .contacts-form{
    background: #2C2450;
    padding: 60px 110px;
    margin: 0px 75px;
    transform: translateY(-40%);
  }

  .form-inputs{
    margin: 30px 0px;
  }

  .contacts-form > h2{
    color: #fff;
  }

  .form-input{
    width: 300px;
    margin-right: 30px;
  }
</style>