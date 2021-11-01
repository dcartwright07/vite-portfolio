<template>
  <div>
    <div class="container mx-auto">
      <AboutMe
        :bio="profile.bio"
        :image="profile.image.url"
        :name="profile.name"
      />
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

import axios from 'axios'

export default {
  name: 'About',

  components: {
    AboutMe,
    AboutCounter,
    Clients,
  },

  data() {
    return {
      profile: {},
    }
  },

  async created() {
    const { data } = await axios.get('http://api.dominiccartwright.com/profile')
    this.profile = data
  },

  async mounted() {
    feather.replace()
  },

  updated() {
    feather.replace()
  },
}
</script>

<style scoped></style>
