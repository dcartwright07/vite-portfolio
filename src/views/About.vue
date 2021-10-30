<template>
  <div>
    <div class="container mx-auto">
      <AboutMe />
    </div>

    <AboutCounter />

    <div class="container mx-auto">
      <Clients />
    </div>
  </div>
</template>

<script>
import AboutMe from '../components/about/AboutMe.vue'
import AboutCounter from '../components/about/AboutCounter.vue'
import Clients from '../components/about/Clients.vue'
import feather from 'feather-icons'

export default {
  name: 'About',

  components: {
    AboutMe,
    AboutCounter,
    Clients,
  },

  mounted() {
    feather.replace()
  },

  updated() {
    feather.replace()
  },
}
</script>

<style scoped></style>
