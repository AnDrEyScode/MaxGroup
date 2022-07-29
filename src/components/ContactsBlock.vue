<template>
  <a name="contacts"></a>
  <div class="contacts" >
    <contacts-form class="contacts-form"/>
    <div class="contacts-container">
      <div class="contacts-content">
        <h2>Наши контакты</h2>
        <p class="contacts-mail"><img src="@/assets/icons/mail.png" alt="mail"> maksgroup@mail.ru</p>
        <p class="contacts-address"><img src="@/assets/icons/location.png" alt="location"> ул. Белая, д 2</p>
        <p class="contacts-phone"><img src="@/assets/icons/phone.png" alt="phone"> 8 (495) 285 12-21</p>
      </div>
      <div class="map">
        <!-- <iframe src="" frameborder="0"></iframe> -->
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2247.813056815686!2d37.351625416334485!3d55.70962118054186!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46b54fb4d51ed1a3%3A0x8bce54b0378ac77c!2z0KDRg9Cx0LvQtdCy0YHQutC40Lkg0L_RgC4sIDYsINCd0LXQvNGH0LjQvdC-0LLQutCwLCDQnNC-0YHQutC-0LLRgdC60LDRjyDQvtCx0LsuLCAxNDMwMjY!5e0!3m2!1sru!2sru!4v1659131713763!5m2!1sru!2sru" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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

  .contacts-form{
    /* transform: translateY(-40%); */
    top: -20%;
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
    min-height: 300px;
  }

  .map iframe{
    width: 100%;
    height: 100%;
  }

  @media screen and (max-width: 800px) {

    .contacts-content p{
      font-weight: 400;
      font-size: 11px;
      line-height: 13px;
    }


  }

  @media screen and (max-width: 600px) {
    .contacts{
      height: auto;
      position: relative;
      margin-top: -60px;
    }

    .contacts-form{
      position: relative;
      margin-top: 60px;
    }

    .contacts-container{
      height: 20%;
      position: relative;
      flex-direction: column;
      justify-content: center;
    }

    .contacts-content{
      width: 90%;
      height: max-content;
      margin: auto;
      align-items: center;
      border: 1px solid black;
      padding: 30px;
    }

    .map{
      position: relative;
      width: 100%;
      z-index: -1;
      border: none;
      border: 1px solid black;
      margin-top: -60px;
    }

    .contacts-content p{
      font-weight: 400;
      font-size: 10px;
      line-height: 12px;
    }

    .contacts-address{
      order: 1;
    }

    .contacts-phone{
      order: 2;
    }

    .contacts-mail{
      order: 3;
    }
  }
</style>