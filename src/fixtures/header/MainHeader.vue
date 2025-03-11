<script setup lang="ts">
import { RouterLink, RouterView, useRoute } from 'vue-router';

const route = useRoute();

const getH2 = (): string => {
  switch (route.path) {
    case '/':
      return '/Tyler, The Creator';
    case '/album':
      return '/album';
    case '/tour':
      return '/tour';
    case '/store':
      return '/store';
    default:
      return '';
  }
};
</script>

<template>
  <header class="header">
    <h1>FLOWER BOY</h1>
    <h2>{{ getH2() }}</h2>

    <input type="checkbox" />

    <div class="menu">
      <button class="burgermenu" id="burgermenu" onclick="burgerMenuFunctionality()">
        <span></span>
        <span></span>
        <span></span>
      </button>

      <nav id="nav">
        <ul class="menu-list" id="menu-list">
          <li><RouterLink to="/">Home</RouterLink></li>
          <li><RouterLink to="/album">Album</RouterLink></li>
          <li><RouterLink to="/tour">Tour</RouterLink></li>
          <li><RouterLink to="/store">Store</RouterLink></li>
        </ul>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
@import 'header.scss';
</style>
