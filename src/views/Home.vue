<template>
  <div class="container mx-auto">
    <Banner />
    <ProjectsGrid />
  </div>
</template>

<script>
import Banner from '../components/home/Banner.vue'
import ProjectsGrid from '../components/project/ProjectsGrid.vue'
import feather from 'feather-icons'

export default {
  name: 'Home',

  components: {
    Banner,
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
}
</script>
