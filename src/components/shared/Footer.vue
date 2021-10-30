<template>
  <footer class="mx-auto">
    <div class="pt-10 pb-8">
      <div class="flex flex-col justify-center items-center mb-6">
        <Logo :imageWidth="400" color="white" />

        <ul class="flex gap-3 sm:gap-8 py-8">
          <a
            v-for="social in socials"
            :key="social.id"
            :href="social.url"
            target="__blank"
            class="text-gray-300 hover:text-gray-100 dark:hover:text-indigo-400 cursor-pointer bg-gray-700 dark:bg-ternary-dark hover:bg-red-700 shadow-sm∫ p-4 rounded-full"
          >
            <i :data-feather="social.icon" class="w-5 h-5"></i>
          </a>
        </ul>
      </div>

      <div
        class="footer-copyright flex justify-center items-center text-center pt-8"
      >
        <div class="text-gray-100 text-sm dark:text-ternary-light">
          &copy; Copyright {{ copyrightDate }}. All Rights Reserved |
          <a
            href="https://dominiccartwright.com"
            target="__blank"
            class="text-red-700 dark:text-secondary-light font-medium uppercase hover:underline"
          >
            Dominic Cartwright
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Logo from './Logo.vue'
import feather from 'feather-icons'

export default {
  components: { Logo },

  data() {
    return {
      copyrightDate: new Date().getFullYear(),
      socials: [
        {
          id: 1,
          name: 'GitHub',
          icon: 'github',
          url: 'https://github.com/dcartwright07',
        },
        {
          id: 2,
          name: 'Twitter',
          icon: 'twitter',
          url: 'https://twitter.com/nickcartwri12',
        },
        {
          id: 3,
          name: 'Facebook',
          icon: 'facebook',
          url: 'https://www.facebook.com/nicholas.cartwright1',
        },
        {
          id: 4,
          name: 'LinkedIn',
          icon: 'linkedin',
          url: 'https://www.linkedin.com/in/dominic-cartwright/',
        },
      ],
    }
  },

  mounted() {
    feather.replace()
  },

  updated() {
    feather.replace()
  },
}
</script>

<style scoped>
footer {
  background: #212529;
  border-top: 4px solid #212529;
  font-size: 0.9em;
  margin-top: 50px;
  padding: 0;
  position: relative;
  clear: both;
}
.footer-copyright {
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}
</style>
