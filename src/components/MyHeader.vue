<template>
  <header class="header">
    <HeaderNav :links="links" />
  </header>
</template>

<script setup>
import HeaderNav from "./Header/HeaderNav.vue";
defineProps({
  links: Array,

})
</script>

<style></style>