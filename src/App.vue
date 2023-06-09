<template>
  <Navbar />
  <router-view />
</template>

<script>
import Navbar from './views/Navbar.vue';

export default {
  components: {
    Navbar
  }
}
</script>

<style>
a:-webkit-any-link {
    color: -webkit-link;
    cursor: pointer;
}
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
</style>