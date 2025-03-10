<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import MainHeader from './fixtures/header/MainHeader.vue';
import MainFooter from './components/MainFooter.vue';

</script>

<template>

<MainHeader />

  <RouterView />

  <MainFooter />
</template>

<style scoped>


</style>
