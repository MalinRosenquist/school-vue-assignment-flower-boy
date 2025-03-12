<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue';

import desktopHero from '@/assets/hero-landing-page-desktop.svg';
import mobileHero from '@/assets/hero-landing-page-mobile.svg';

const imageSrc = ref<string>(mobileHero);

const updateHero = () => {
  if (window.innerWidth <= 1440) {
    imageSrc.value = mobileHero;
  } else {
    imageSrc.value = desktopHero;
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
    <img
      :src="imageSrc"
      class="hero-image"
      alt="Illustraded image of a sunrise above a bed of sunflowers, with bees flying among the clouds. Tyler the Creator is depicted riding on top of one of the bees."
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
body {
  background-color: $bg-yellow;
}

.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
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
