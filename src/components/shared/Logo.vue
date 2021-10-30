<template>
  <img :src="image" :width="imageWidth" alt="Dominic Cartwright Logo" />
</template>

<script>
import WhiteLogo from '../../assets/images/logo-w.svg'
import BlackLogo from '../../assets/images/logo.svg'

export default {
  props: {
    imageWidth: {
      type: Number,
      default: 200,
    },
    color: {
      type: String,
      default: 'black',
    },
  },

  computed: {
    image() {
      return this.color === 'white' ? WhiteLogo : BlackLogo
    },
  },
}
</script>
