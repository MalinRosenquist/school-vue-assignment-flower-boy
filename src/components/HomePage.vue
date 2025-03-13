<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue';

import AlbumMobile from './albumcover/AlbumMobile.vue';
import AlbumDesktop from './albumcover/AlbumDesktop.vue';

const currentComponent = ref<typeof AlbumMobile | typeof AlbumDesktop>(AlbumMobile);

const updateHero = () => {
  if (window.innerWidth <= 1440) {
    currentComponent.value = AlbumMobile;
  } else {
    currentComponent.value = AlbumDesktop;
  }
};

onMounted(() => {
  updateHero();
  window.addEventListener('resize', updateHero);
});

onBeforeUnmount(() => {
  window.removeEventListener('resize', updateHero);
});
</script>

<template class="home-page">
  <section class="hero-container">
    <component
      :is="currentComponent"
      alt="An illustrated image of a sunrise over a bed of sunflowers. Bees are flying among the clouds with Tyler riding on one of them"
    />
  </section>
  <div class="wrapper">
    <section class="intro-text">
      <h2>21.07.2017</h2>
      <p>
        Welcome to Flower Boy — a world where introspection meets vibrant soundscapes. Tyler, The
        Creator’s fourth studio album blends lush production with raw lyricism, exploring themes of
        love, identity, and self-growth. Immerse yourself in a sonic journey filled with soul, jazz,
        and hip-hop influences, crafted with Tyler’s signature artistry. Experience the album, dive
        into behind-the-scenes moments, and grab exclusive merch. Let Flower Boy bloom.
      </p>
    </section>
  </div>
  <section class="bee-container">
    <img
      src="@/assets/bee.svg"
      class="bee-image"
      alt="Illustrated image of a bee with in yellow awith black stripes."
    />
  </section>
</template>

<style scoped lang="scss">
.hero-container {
  width: 100%;
  background: linear-gradient(to bottom, transparent 0%, $bg-dark-green 100%);
}

.intro-text {
  color: $font-primary;
  background-color: $bg-dark-green;
  padding: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;

  h2 {
    color: $font-tertiery;
  }

  p {
    font-size: 1.25rem;
    max-width: 610px;
  }
}

.bee-container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
  background-color: $bg-dark-green;

  img {
    max-width: 107px;
  }
}

/* ----------------------*/
/* ----`*~ DESKTOP ~*´----*/
/* ----------------------*/

@media screen and (min-width: 1440px) {
  .wrapper {
    position: relative;
    height: 200px;
    background-color: $bg-dark-green;
  }
  .intro-text {
    position: absolute;
    top: -180px;
    left: 50%;
    transform: translate(-50%);
    z-index: 1;

    p {
      max-width: 912px;
    }
  }

  .bee-container {
    display: none;
  }
}
</style>
