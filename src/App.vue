<template>
  <div class="wrapper">
    <MyHeader :links="links" />
    <MyMain />
    <MyFooter :footerLinks="links" />
  </div>
</template>

<script setup>
import MyHeader from "@/components/MyHeader.vue";
import MyFooter from "@/components/MyFooter.vue";
import MyMain from "@/components/MyMain.vue";


import { ref, onMounted } from "vue";

const isActive = ref(false)

const closeDropDown = () => {
  if (isActive) {
    isActive.value = false
  }
}


const links = [
  { id: 1, name: "Home", path: '#home', imageUrl: '/images/home.svg' },
  { id: 1, name: "About Me", path: '#about', imageUrl: '/images/user.svg' },
  { id: 1, name: "Projects", path: '#projects', imageUrl: '' },
  { id: 1, name: "Skills", path: '#skills', imageUrl: '' },
  { id: 1, name: "Contact", path: '#contact', imageUrl: '/images/phone.svg' },
];

// const screenWidth = ref(screen.width);

onMounted(() => {
  // console.log(screenWidth.value);
})

</script>

<style></style>
