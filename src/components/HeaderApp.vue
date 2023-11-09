<template>
  <header class="text-center my-4">
    <img src="../assets/images/la-molisana-logo.png" alt="Logo">
    <NavBar />
  </header>
</template>

<script>
import NavBar from './header/NavBar.vue'
export default {
  name: 'HeaderApp',
  components: {
    NavBar
  }

}
</script>

<style lang="scss" scoped></style>