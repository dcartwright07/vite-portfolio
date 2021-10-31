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
const projectImages = import.meta.glob(
  '/src/assets/images/projects/*.@(jpg|png)',
)

export default {
  data() {
    return {
      projectImages: [
        {
          id: 1,
          title: 'Kabul Project Management UI',
          img: this.imageUrl('ui-project-1.jpg'),
        },
        {
          id: 2,
          title: 'Kabul Project Management UI',
          img: this.imageUrl('web-project-2.jpg'),
        },
        {
          id: 3,
          title: 'Kabul Project Management UI',
          img: this.imageUrl('mobile-project-2.jpg'),
        },
      ],
    }
  },

  methods: {
    imageUrl(value) {
      const imageArray = Object.values(projectImages)
      const imageUrl = imageArray.find(
        (image) => image.name.split('/')[5] === value,
      )
      return imageUrl.name
    },
  },
}
</script>
