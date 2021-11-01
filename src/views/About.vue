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
      <Clients :clients="clients" />
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
      clients: [],
    }
  },

  async created() {
    const profileData = await axios.get(
      'http://api.dominiccartwright.com/profile',
    )
    this.profile = profileData.data
    const clientData = await axios.get(
      'http://api.dominiccartwright.com/clients',
    )
    this.clients = clientData.data
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
