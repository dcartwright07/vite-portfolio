<template>
  <header class="px-8 py-2 border-b">
    <div class="flex justify-between items-center">
      <a href="/">
        <Logo />
      </a>

      <nav class="collapse flex flex-row space-x-6">
        <a href="/" class="current text-gray-500 hover:text-red-700">
          Porfolio
        </a>
        <a href="/about" class="text-gray-500 hover:text-red-700">
          About
        </a>
        <a href="/contact" class="text-gray-500 hover:text-red-700">
          Contact
        </a>
      </nav>
    </div>
  </header>
</template>

<script>
import Logo from './Logo.vue'

export default {
  components: { Logo },
}
</script>

<style scoped>
header {
  -webkit-transition: ease height 300ms;
  transition: ease height 300ms;
}
</style>
