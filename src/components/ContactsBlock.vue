<template>
  <div class="contacts">
    <contacts-form/>
    <div class="contacts-container">
      <div class="contacts-content">
        <h2>Наши контакты</h2>
        <p><img src="@/assets/icons/mail.png" alt="mail"> maksgroup@mail.ru</p>
        <p><img src="@/assets/icons/location.png" alt="location"> ул. Белая, д 2</p>
        <p><img src="@/assets/icons/phone.png" alt="phone"> 8 (495) 285 12-21</p>
      </div>
      <div class="map">
        <iframe src="" frameborder="0"></iframe>
      </div>
    </div>
  </div>
</template>

<script>
import ContactsForm from './ContactsForm.vue'
export default {
  components: {
    ContactsForm
  }
}
</script>

<style>
  .contacts{
    height: 80vh;
    width:100%;
    position: relative;
  }

  .contacts-container{
    height: 70%;
    width: 100%;
    position: absolute;
    bottom: 0;
    left: 0;
    display: flex;
    align-items: center;
  }

  .contacts-content{
    margin-left: 75px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    height: 100%;
    width: calc(35% - 75px);
    color: #2C2450;
  }

  .contacts-content h2{
    margin-bottom: 20px;
  }

  .contacts-content img{
    width: 20px;
    height: auto;
    margin-right: 10px;
  }

  .contacts-content p{
    display: flex;
    align-items: center;
    margin: 10px 0px;
  }

  .map{
    width: 65%;
    height: 100%;
    border: 1px solid black;
  }

  @media screen and (max-width: 800px) {

    .contacts-content p{
      font-weight: 400;
      font-size: 11px;
      line-height: 13px;
    }
  }

  @media screen and (max-width: 480px) {
    .contacts-container{
      height: 70%;
      position: absolute;
      bottom: 0;
      left: 0;
      flex-direction: column;
    }

    .contacts-content{
      width: 90%;
      height: 40%;
      margin: auto;
      align-items: center;
      transform: translateY(50%);
      border: 1px solid black;
    }

    .map{
      width: 100%;
      height: 70%;

    }

    .contacts-content p{
      font-weight: 400;
      font-size: 10px;
      line-height: 12px;
    }
  }
</style>