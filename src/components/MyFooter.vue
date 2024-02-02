<template>
  <footer class="footer">
    <FooterList>
      <!-- <list-link v-for="link in footerLinks" :key="link.id" :link="link" :show-img="true"
        class="footer__nav-list-link nav__link" /> -->
    </FooterList>
    <FooterList style="gap: 24px;">
      <LinkIcon v-for="item in iconLinks" :key="item.id" :item="item" />
    </FooterList>
    <h6 class="footer__policy">Terms of Service - Privacy Policy</h6>
  </footer>
</template>

<script setup>
import ListLink from '@/components/UI/ListLink.vue';
import LinkIcon from '@/components/UI/LinkIcon.vue';
import FooterList from '@/components/Footer/FooterList.vue';

defineProps({
  footerLinks: Array,
});

const iconLinks = [
  { id: 1, imgPath: '/images/facebook.svg', altName: 'facebook' },
  { id: 2, imgPath: '/images/instagram.svg', altName: 'instagram' },
  { id: 3, imgPath: '/images/twitter.svg', altName: 'twitter' },
  { id: 4, imgPath: '/images/youtube.svg', altName: 'youtube' },
];

</script>

<style lang="scss">
.footer {
  padding-top: 110px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 46px;

  @media (max-width:479.99px) {
    gap: 15px;
    padding-top: 50px;

  }

  &__nav {

    &-link {
      display: flex;
      align-items: center;
      gap: 10px;
      filter: brightness(0.9);
    }


  }

  &__policy {
    color: rgba(238, 238, 238, 0.75);
    font-size: 18px;
    font-weight: 400;
    padding: 48px 96px;
    display: flex;
    align-self: flex-end;

    @media (max-width:479.99px) {
      font-size: 12px;
      padding: 25px 25px;
    }

    @media (max-width:319.99px) {
      font-size: 10px;

    }
  }
}
</style>