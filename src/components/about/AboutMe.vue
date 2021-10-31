<template>
  <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
    <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
      <img :src="ProfileImage" class="rounded-xl w-96" alt="" />
    </div>
    <div class="w-full sm:w-3/4 text-left">
      <p
        v-for="bio in bios"
        :key="bio.id"
        class="mb-4 text-ternary-dark dark:text-ternary-light text-lg"
      >
        {{ bio.bio }}
      </p>
    </div>
  </div>
</template>

<script>
import ProfileImage from '../../assets/images/profile-square.jpg'

export default {
  setup() {
    return {
      bios: [
        {
          id: 1,
          bio:
            "I seek to provide web solutions for companies and non-profit organizations that will enhance their vision and achieve their goals. I am also a technology enthusiast, philosophical thinker, and people-lover. Being of Caribbean descent, I like to chill to reggae tunes and I get really excited when I'm talking to people.",
        },
      ],
    }
  },
}
</script>
