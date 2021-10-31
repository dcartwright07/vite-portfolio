<template>
  <section class="pt-20 sm:pt-28">
    <div class="text-center">
      <p
        class="text-2xl sm:text-5xl font-semibold mb-3 text-ternary-dark dark:text-ternary-light"
      >
        Projects Portfolio
      </p>
      <p class="text-md sm:text-xl text-gray-500 dark:text-ternary-light">
        Some of the projects I have successfully completed
      </p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-3 mt-16 sm:gap-10">
      <router-link
        v-for="project in projects"
        :key="project.id"
        to="/projects/single-project"
        class="rounded-3xl shadow-lg hover:shadow-xl cursor-pointer mb-10 sm:mb-0 bg-secondary-light dark:bg-ternary-dark"
        aria-label="Single Project"
      >
        <div>
          <img
            :src="project.img"
            :alt="project.title"
            class="rounded-t-3xl border-none"
          />
        </div>
        <div class="text-center px-4 py-6">
          <p
            class="text-2xl text-ternary-dark dark:text-ternary-light font-semibold mb-2"
          >
            {{ project.title }}
          </p>
          <span class="text-lg text-ternary-dark dark:text-ternary-light">
            {{ project.category }}
          </span>
        </div>
      </router-link>
    </div>

    <div class="mt-10 sm:mt-20 flex justify-center">
      <router-link
        to="/projects"
        class="flex items-center px-6 py-3 rounded-xl shadow-lg hover:shadow-xl bg-red-700 hover:bg-red-800 focus:ring-1 focus:ring-indigo-900 text-white text-lg sm:text-xl font-medium"
        aria-label="More Projects"
      >
        More Projects
      </router-link>
    </div>
  </section>
</template>

<script>
import feather from 'feather-icons'

import WebProject1 from '../../assets/images/projects/web-project-1.jpg'
import WebProject2 from '../../assets/images/projects/web-project-2.jpg'
import MobileProject1 from '../../assets/images/projects/mobile-project-1.jpg'
import MobileProject2 from '../../assets/images/projects/mobile-project-2.jpg'
import UIProject1 from '../../assets/images/projects/ui-project-1.jpg'
import UIProject2 from '../../assets/images/projects/ui-project-2.jpg'

export default {
  name: 'Projects',

  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Google Health Platform',
          category: 'Wen Application',
          img: WebProject2,
        },
        {
          id: 2,
          title: 'Pheonix Digital Agenncy',
          category: 'Mobile Application',
          img: MobileProject2,
        },
        {
          id: 3,
          title: 'Project Management UI',
          category: 'UI / Frontend',
          img: UIProject1,
        },
        {
          id: 4,
          title: 'Cloud Storage Platform',
          category: 'UI / Frontend',
          img: UIProject2,
        },
        {
          id: 5,
          title: 'Kabul Social App',
          category: 'Mobile Application',
          img: MobileProject1,
        },
        {
          id: 6,
          title: 'Apple Design System',
          category: 'Web Application',
          img: WebProject1,
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
