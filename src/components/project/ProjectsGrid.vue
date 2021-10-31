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

import TaylorUniversity from '../../assets/images/projects/taylor.jpg'
import BGCMarion from '../../assets/images/projects/bgc-marion.png'
import MissionPoint from '../../assets/images/projects/missionpoint.jpg'
import PositivelyBlackford from '../../assets/images/projects/positivelyblackford.jpg'
import HamiltonEyecare from '../../assets/images/projects/hamilton-eyecare.jpg'
import TiptonCountyIn from '../../assets/images/projects/tipton-county-in.png'

export default {
  name: 'Projects',

  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Community Engagement',
          category: 'Website',
          img: BGCMarion,
        },
        {
          id: 2,
          title: 'Digital News Outlet',
          category: 'Website',
          img: PositivelyBlackford,
        },
        {
          id: 3,
          title: 'Optometry Office',
          category: 'Website',
          img: HamiltonEyecare,
        },
        {
          id: 4,
          title: 'Community Foundation',
          category: 'Website',
          img: TiptonCountyIn,
        },
        {
          id: 5,
          title: 'Church Community Engagement',
          category: 'Website',
          img: MissionPoint,
        },
        {
          id: 6,
          title: 'Lead Generation Platform',
          category: 'Web Application',
          img: TaylorUniversity,
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
