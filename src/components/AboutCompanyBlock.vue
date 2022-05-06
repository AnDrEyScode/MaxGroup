<template>
  <a name="about"></a>
  <div class="about-company">
    <div class="about-company-content">
      <h2>О нашей компании</h2>
      <p>
        Компания «Макс Групп» — это собственное производство уличной мебели и малых архитектурных форм (МАФ), помощь в разработке проектов по благоустройству городских и частных территорий. Мы стараемся предложить наиболее эффективные и выгодные решения. Все проекты на стадии разработки, согласования и реализации выполняются под четким контролем, в нужные сроки и в рамках обозначенного бюджета. Имея собственное производство уличной мебели, мы имеем возможность предоставить конкурентоспособные цены и стать для вас надежным и выгодным партнером. Наши специалисты всегда рады предложить хорошие, свежие и выгодные решения, помочь с выбором.
      </p>
      <div class="read-more" @click="showMore">
        <img :src="require('@/assets/icons/readMore.png')" alt="arrow">
        <span>Читать ещё</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    showMore(){
      document.querySelector('.about-company-content').classList.toggle('content-full')
    }
  }
}
</script>

<style scoped>
  .about-company{
    height: 80vh;
    background-image: url("@/assets/background/about.png");
    background-repeat: no-repeat;
    background-size:cover;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color:#fff;
  }

  .about-company-content{
    position: relative;
    left: 40%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 40%;
  }

  .about-company-content > h2{
    margin-bottom: 40px;
  }

  .about-company-content > p{
    margin-bottom: 30px;
    height: 110px;
    overflow: hidden;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 22px;
    transition: height 0.7s;
  }

  .read-more:hover{
    cursor: pointer;
  }

  .read-more > span{
    margin-left: 10px;
  }

  .read-more > img{
    width: 8px;
  }

  .content-full > p{
    height:20vh;
    
  }

  .content-full > .read-more > img{
    transform: rotateZ(90deg);
  }

  @media screen and (max-width: 800px) {
    .about-company-content{
      left: 20%;
      width: 60%;
    }

    .about-company-content > h2{
      font-weight: 600;
      font-size: 30px;
      line-height: 37px;
    }

    .about-company-content > p{
      font-weight: 400;
      font-size: 16px;
      line-height: 20px;
    }

    .read-more > span{
      font-weight: 600;
      font-size: 10px;
      line-height: 12px;
    }
  }

  @media screen and (max-width: 480px) {
    .about-company{
      height: 100vh;
    }

    .about-company-content > h2{
      font-weight: 600;
      font-size: 20px;
      line-height: 24px;
    }

    .about-company-content > p{
      font-weight: 400;
      font-size: 10px;
      line-height: 12px;
    }

    .read-more > span{
      font-weight: 600;
      font-size: 8px;
      line-height: 10px;
    }
  }
</style>