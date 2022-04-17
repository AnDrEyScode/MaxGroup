<template>
  <div class="projects">
    <h2>Выполненные проекты</h2>
    <projects-list :projects="projects"/>
    <my-button class="blue" :value="'Показать ещё'"/>
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

}
</script>

<style scoped>
  .projects{
    height: max-content;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 75px;
  }
</style>