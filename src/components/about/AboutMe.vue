<template>
  <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
    <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
      <img :src="profileImage" class="rounded-xl w-96" :alt="name" />
    </div>
    <div class="w-full sm:w-3/4 text-left">
      <p class="mb-4 text-ternary-dark dark:text-ternary-light text-lg">
        {{ bio }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bio: {
      type: String,
      requied: true,
    },
    image: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },

  computed: {
    profileImage() {
      return 'http://api.dominiccartwright.com' + this.image
    },
  },
}
</script>
