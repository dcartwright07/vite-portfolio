<template>
  <div
    class="mt-10 pt-10 sm:pt-14 sm:mt-20 border-t-2 border-primary-light dark:border-secondary-dark"
  >
    <p
      class="text-primary-dark dark:text-primary-light text-3xl font-bold mb-10 sm:mb-14 text-left"
    >
      Related Projects
    </p>

    <div class="grid grid-cols-1 sm:grid-cols-4 gap-10">
      <div>
        <img
          :src="MobileProject2"
          class="rounded-2xl cursor-pointer"
          alt="Related Project"
        />
      </div>
      <div>
        <img
          :src="WebProject1"
          class="rounded-2xl cursor-pointer"
          alt="Related Project"
        />
      </div>
      <div>
        <img
          :src="UIProject2"
          class="rounded-2xl cursor-pointer"
          alt="Related Project"
        />
      </div>
      <div>
        <img
          :src="MobileProject1"
          class="rounded-2xl cursor-pointer"
          alt="Related Project"
        />
      </div>
    </div>
  </div>
</template>

<script>
import WebProject1 from '../../assets/images/projects/web-project-1.jpg'
import MobileProject1 from '../../assets/images/projects/mobile-project-1.jpg'
import MobileProject2 from '../../assets/images/projects/mobile-project-2.jpg'
import UIProject2 from '../../assets/images/projects/ui-project-2.jpg'

export default {
  setup() {},
}
</script>
