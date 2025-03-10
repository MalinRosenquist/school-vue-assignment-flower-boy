<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
</script>

<template>
<header class="header">
<h1>FLOWER BOY</h1>
<h2>/Tyler, The Creator</h2>
  <div class="menu">    
    <button class="burgermenu" id="burgermenu">        
      <span></span>
      <span></span>
      <span></span>
    </button>

    <nav id="nav">
      <ul class="menu-list">
        <li><RouterLink to="/">Home</RouterLink></li>
        <li><RouterLink to="/album">Album</RouterLink></li>
        <li><RouterLink to="/tour">Tour</RouterLink></li>
        <li><RouterLink to="/store">Store</RouterLink></li>
      </ul> 
    </nav>
  </div> 
</header>

<main>
  <RouterView />
</main>
</template>

<style scoped>
@import 'header.scss';
</style>