<template>
  <div class="grid grid-cols-1 sm:grid-cols-3 sm:gap-10 mt-12">
    <div
      class="mb-10 sm:mb-0"
      v-for="projectImage in projectImages"
      :key="projectImage.id"
    >
      <img
        :src="projectImage.img"
        class="rounded-2xl cursor-pointer shadow-lg sm:shadow-none"
        alt="{{ projectImage.title }}"
      />
    </div>
  </div>
</template>

<script>
import WebProject2 from '../../assets/images/projects/web-project-2.jpg'
import MobileProject2 from '../../assets/images/projects/mobile-project-2.jpg'
import UIProject1 from '../../assets/images/projects/ui-project-1.jpg'

export default {
  data() {
    return {
      projectImages: [
        {
          id: 1,
          title: 'Kabul Project Management UI',
          img: UIProject1,
        },
        {
          id: 2,
          title: 'Kabul Project Management UI',
          img: WebProject2,
        },
        {
          id: 3,
          title: 'Kabul Project Management UI',
          img: MobileProject2,
        },
      ],
    }
  },
}
</script>
