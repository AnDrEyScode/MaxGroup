<template>
  <div class="project" @mouseover="showShortInfo" @mouseleave="hideShortInfo">
    <img :src="project.path" alt="project-IMG" class="project-img">
    <div class="project-content">
      <h3>{{ project.title }}</h3>
      <p class="address">{{ project.address }}</p>
      <p>{{ project.body }}</p>

      
      <div class="project-phases">

        <div class="phase-list">
          <p>Были проведены следующие этапы:</p>
          <ul>
            <li class="phase-item" v-for="phase in project.phases" :key="Date.now() + phase.length">{{ phase }}</li>
          </ul>
        </div>

        <div class="count-charecters">
          <div class="time-span"><img :src="require('@/assets/icons/time.png')" alt="clock"> {{ project.timespan }}</div>
          <div class="cost"><img :src="require('@/assets/icons/price.png')" alt="$"> {{ project.price }} ₽</div>
        </div>

      </div>
      <my-button :value="'Скрыть'" @click="hideFull" class="blue hidebtn"/>
      <my-button :value="'Подробнее'" @click="showFull" class="blue showbtn"/>

    </div>
  </div>
</template>

<script>
import MyButton from './UI/MyButton.vue';
export default {
  components: { MyButton },
  props: {
    project: {
      type: Object,
      required: true
    },
  },

  data(){
    return {
      isFullView: false
    }
    
  },

  methods: {
    showShortInfo(){
      if(this.isFullView)
        return

      this.$el.querySelector(".project-content").classList.add('project-content-short-view')
    },

    hideShortInfo(){
      if(this.isFullView)
        return

      this.$el.querySelector(".project-content").classList.remove('project-content-short-view')
    },

    showFull(){
      this.isFullView = true
      // content = this.$el.querySelector(".project-content")
      this.$el.querySelector(".project-content").classList.remove('project-content-short-view')
      this.$el.querySelector(".project-content").classList.add('project-content-full-view')
    },

    hideFull(){
      this.isFullView = false
      this.$el.querySelector(".project-content").classList.remove('project-content-full-view')
    }
  }
}
</script>

<style scoped>
  .project{
    position: relative;
    height: 450px;
    display: flex;
    flex-wrap: nowrap;
    overflow: hidden;
    /* max-width: 630px; */
    margin: 10px 5px;
  }

  .project-img{
    position: relative;
    width: 100%;
    height: 100%;
    
    max-width: 630px;
  }

  .project-content{
    display: flex;
    flex-direction: column;
    align-items: left;
    justify-content: space-between;
    position: absolute;
    left: 0;
    top: 0;
    /* flex: 0 0 50%; */
    background: rgba(17, 6, 68, 0.3);
    backdrop-filter: blur(2px);
    transform: translateY(80%);
    width: 100%;
    height: 100%;
    max-width: 630px;
    padding: 10px 20px;
  }

  

  .project p{
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 17px;
  }


  .project-phases{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .phase-list > p{
    font-weight: 600;
  }

  .phase-list > ul{
    list-style-position: inside;
    margin: 20px 0px;
  }

  .count-charecters img{
    height: 20px;
    margin-right: 10px;
  }

  .project-content > *{
    /* text-align: left; */
    display: none;
  }

  .project-content > h3{
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    display: block;
    color: #FFFFFF;
  }




  .project-content-short-view{
    width: 60%;
    left: 40%;
    transform: none;
    padding: 30px;
    justify-content: center;
    
  }

  .project-content-short-view *{
    color: #FFFFFF;
    
  }

  .project-content-short-view > h3{
    display: block;
    margin: 20px 0px;
  }

  .project-content-short-view > .address{
    display: block;
    order: -1;
  }

  .project-content-short-view > .project-phases{
    display: block;
  }

  .project-content-short-view .phase-list{
    display: block;
  }

  .project-content-short-view .phase-list > *{
    display: none;
  }

  .project-content-short-view .count-charecters{
    display: flex;
    margin: 10px 0px;
    justify-content: space-between;
  }

  .project-content-short-view .count-charecters > div{
    display: flex;
    align-items: center;
  }

  .project-content-short-view > .showbtn{
    display: block;
    text-align: center;
    align-self: center;
    width: 90%;
    margin-top: 20px;
  }

  



  .project-content-full-view{
    transform: none;
    background: #FFFFFF;
    position: relative;
    display: flex;
  }

  .project-content-full-view > *{
    display: flex;
  }

  .project-content-full-view > h3{
    font-style: normal;
    font-weight: 600;
    font-size: 30px;
    line-height: 37px;
    color: #2C2450;
  }

  .project-content-full-view > p{
    margin: 10px 0px;
    color: #2C2450;
  }

  .project-content-full-view > .phase-list{
    margin: 20px;
  }

  .project-content-full-view .count-charecters{
    margin-right: 70px;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: left;
  }

  .project-content-full-view .count-charecters > div{
    display: flex;
    align-items: center;
  }

  .project-content-full-view > .showbtn{
    display: none;
  }

  .project-content-full-view > .hidebtn{
    display: block;
    width:50%;
    text-align: center;
  }






</style>