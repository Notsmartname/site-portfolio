<template>
  <li>
    <a class="header__nav-list-link nav__link" :href="link.path">
      <img v-if="showImg" :src="link.imageUrl" :alt="link.name" />
      {{ link.name }}
    </a>
  </li>
</template>

<script setup>
defineProps({
  link: Object,
  showImg: Boolean,
});
</script>

<style lang="scss">
.nav__link {
  cursor: pointer;
  // margin-left: 48px;
  color: var(--mainColorText);
  font-family: "Poppins";
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  display: flex;
  align-items: center;
  gap: 10px;
}

.nav__link:hover {
  color: var(--subMainColorText);
}
</style>