<template>
  <div class="projects-list">
    <project-item v-for="proj in projects" :key="proj.id"/>
  </div>
</template>

<script>
import ProjectItem from '@/components/ProjectItem.vue'
export default {
  components: {
    ProjectItem
  },
  props: {
    projects: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>

</style>