<template>
  <div class="header">
    <nav class="header__nav container">
      <a href="#" class="header__nav-logo"> WebDeveloper </a>
      <ul class="header__nav-list" v-if="screenWidth > 956">
        <list-link v-for=" link  in  props.links " :key="link.id" :link="link" :show-img="false" class="nav__link" />
      </ul>

      <DropDown :links="links" v-else />
    </nav>
    <LineButton />
  </div>
</template>

<script setup>
import LineButton from '@/components/UI/LineButton.vue';
import ListLink from '@/components/UI/ListLink.vue';
import DropDown from '@/components/UI/DropDown.vue';

import { ref } from 'vue';

const props = defineProps({
  links: Array,
})

const screenWidth = ref(window.innerWidth);


window.addEventListener('resize', () => {
  screenWidth.value = window.innerWidth;
});



</script>

<style lang="scss" scoped>
.header {
  position: fixed;
  width: 100%;
  z-index: 99;
  background: var(--colorBg);


  &__nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 48px;
    padding-bottom: 48px;
    position: relative;

    @media (max-width:955.99px) {
      font-size: 18px;
      padding: 0 15px;
    }

    &-list {
      display: flex;
      gap: 48px;
      align-items: center;
    }

    & a {
      color: var(--mainColorText);
      font-size: 24px;
      font-weight: 700;

      @media (max-width:1199.99px) {
        font-size: 22px;

      }

      @media (max-width:991.99px) {
        font-size: 18px;

      }
    }
  }
}

@media (max-width:1199.99px) {
  .header__nav {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    padding-top: 16px;
    padding-bottom: 16px;
    position: relative;

    &-list {
      display: flex;
      gap: 22px;
      align-items: center;
    }

    &-logo {
      color: var(--mainColorText);
      font-size: 24px;
      font-weight: 700;
    }
  }
}
</style>
