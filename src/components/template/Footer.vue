<template>
  <footer>
    <div class="container pt-10 pb-8 flex justify-center">
      <div class="flex flex-col">
        <Logo :imageWidth="300" color="white" />
        <SocialIcons class="mt-5 mb-5" />
      </div>
    </div>
    <div class="footer-copyright flex justify-center">
      <p class="text-gray-100 py-8 text-xs">
        &copy; Copyright 2020. All Rights Reserved | Dominic Cartwright
      </p>
    </div>
  </footer>
</template>

<script>
import Logo from './Logo.vue'
import SocialIcons from './SocialIcons.vue'

export default {
  components: { Logo, SocialIcons },
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
