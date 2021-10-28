<template>
  <header class="px-8 py-2 border-b">
    <div class="flex justify-between items-center">
      <a href="/">
        <Logo />
      </a>

      <Menu />
    </div>
  </header>
</template>

<script>
import Logo from './Logo.vue'
import Menu from './Menu.vue'

export default {
  components: { Logo, Menu },
}
</script>

<style scoped>
header {
  -webkit-transition: ease height 300ms;
  transition: ease height 300ms;
}
</style>
