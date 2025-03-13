<script setup lang="ts">
import { useRoute } from 'vue-router';
import { onMounted, watch } from 'vue';
import MainHeader from './fixtures/header/MainHeader.vue';
import MainFooter from './fixtures/footer/MainFooter.vue';
import CookieBar from './components/cookiebar/CookieBar.vue';

const route = useRoute();

const updateBackgroundColor = () => {
  document.body.classList.remove('home-page', 'tour-page');

  switch (route.name) {
    case 'home':
      document.body.classList.add('home-page');
      break;
    case 'tour':
      document.body.classList.add('tour-page');
      break;
    default:
      break;
  }
};

onMounted(() => {
  updateBackgroundColor();
});

watch(route, () => {
  updateBackgroundColor();
});
</script>

<template>
  <MainHeader />
  <CookieBar />
  <MainFooter />
</template>

<style lang="scss">
.home-page {
  background-color: $bg-yellow;
}

.tour-page {
  background-color: $bg-light-blue;
}

footer {
  bottom: 0;
}
</style>
