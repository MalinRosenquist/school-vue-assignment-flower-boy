<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
</script>

<template>
<header class="header">
<h1>FLOWER BOY</h1>
<h2>/Tyler, The Creator</h2>

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
</template>

<style scoped>
@import 'header.scss';
</style>