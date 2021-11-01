<template>
  <div class="mt-10 sm:mt-20">
    <p
      class="text-2xl sm:text-4xl text-primary-dark dark:text-primary-light font-sans font-semibold"
    >
      Some of the clients I worked with
    </p>
    <div class="grid grid-cols-2 sm:grid-cols-4 mt-10 sm:mt-20 gap-2">
      <div v-for="client in clients" :key="client.id">
        <img
          :src="profileImage(client.logo.url)"
          :alt="client.name"
          class="w-64 py-5 px-10 border border-ternary-light dark:border-ternary-dark shadow-sm rounded-xl mb-8 cursor-pointer"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    clients: {
      type: Array,
      required: true,
    },
  },

  methods: {
    profileImage(value) {
      return 'http://api.dominiccartwright.com' + value
    },
  },
}
</script>
