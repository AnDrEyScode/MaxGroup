<template>
  <div class="projects">
    <h2>Выполненные проекты</h2>
    <projects-list :projects="projects"/>
    <my-button class="blue projects-btn" :value="'Показать ещё'"/>
  </div>
</template>

<script>
import ProjectsList from '@/components/ProjectsList.vue'
export default {
  components: { ProjectsList },
  data(){
    return {
      projects: []
    }
  },

  mounted(){
     fetch('data/projects.json')
     .then(response => response.json())
     .then(json => this.projects = json.projects)
     .catch(e => console.log(e))
  }

}
</script>

<style scoped>
  .projects{
    height: max-content;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0px 75px;
  }

  .projects > h2{
    margin: 70px auto;
  }

  .projects-btn{
    margin: 30px 0px 90px 0px;
  }
</style>