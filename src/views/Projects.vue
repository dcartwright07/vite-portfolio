<template>
  <div class="container mx-auto">
    <ProjectsGrid />
  </div>
</template>

<script>
import ProjectsGrid from '../components/project/ProjectsGrid.vue'
import feather from 'feather-icons'

export default {
  name: 'Projects',
  components: {
    ProjectsGrid,
  },
  data: () => {
    return {}
  },
  mounted() {
    feather.replace()
  },
  updated() {
    feather.replace()
  },
  methods: {},
}
</script>

<style scoped></style>
