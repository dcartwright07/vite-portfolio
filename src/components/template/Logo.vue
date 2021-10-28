<template>
  <img
    src="/src/assets/logo.svg"
    :width="imageWidth"
    alt="Dominic Cartwright Logo"
  />
</template>

<script>
export default {
  props: {
    imageWidth: {
      type: Number,
      default: 200,
    },
  },
}
</script>
