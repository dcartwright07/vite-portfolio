<template>
  <img :src="image" :width="imageWidth" alt="Dominic Cartwright Logo" />
</template>

<script>
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
      return this.color === 'white'
        ? '/src/assets/logo-w.svg'
        : '/src/assets/logo.svg'
    },
  },
}
</script>
