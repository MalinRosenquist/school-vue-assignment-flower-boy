<script setup lang="ts">
//import { RouterLink, RouterView } from 'vue-router';
import MainHeader from './fixtures/header/MainHeader.vue';
import MainFooter from './fixtures/footer/MainFooter.vue';
import CookieBar from './components/cookiebar/CookieBar.vue';
</script>

<template>
  <MainHeader />

  <!--<RouterView />-->

  <CookieBar />

  <MainFooter />
</template>

<style scoped></style>
