<script setup lang="ts">
import { computed } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();

const currentYear = new Date().getFullYear();

const footerClass = computed(() => {
  return route.path === '/' ? 'footer-dark-green' : 'footer-light-green';
});

const isHomePage = computed(() => {
  return route.path === '/';
});
</script>

<template>
  <footer :class="footerClass">
    <section class="social-media-icons">
      <img src="@/components/icons/spotify.svg" alt="Spotify icon" />
      <img src="@/components/icons/instagram.svg" alt="Instagram icon" />
      <img src="@/components/icons/facebook.svg" alt="Facebook icon" />
      <img src="@/components/icons/twitter.svg" alt="Twitter icon" />
    </section>
    <section class="footer-info">
      <a
        href="mailto:press@tylerthecreator.com"
        aria-label="Click to send an email to press@tylerthecreator.com"
        >Press: press@tylerthecreator.com</a
      >
      <p>&copy;copyright {{ currentYear }}</p>
    </section>
    <section class="flower">
      <img
        :class="{ 'show-flower-mobile': !isHomePage }"
        class="flower-mobile"
        src="@/assets/footer-sunflower-mobile.svg"
        alt="Yellow sunflower"
      />
      <img
        class="flower-desktop"
        src="@/assets/footer-sunflower-desktop.svg"
        alt="Yellow sunflower"
      />
    </section>
  </footer>
</template>

<style scoped lang="scss">
/* ----------------------*/
/* ----`*~ MOBILE ~*´----*/
/* ----------------------*/

.footer-dark-green,
.footer-light-green {
  min-height: 180px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
}

.footer-dark-green {
  background-color: $bg-dark-green;
}

.footer-light-green {
  background-color: $bg-light-green;
}

.social-media-icons {
  display: flex;
  gap: 5vw;
  margin: 20px;

  img {
    max-width: 45px;
    height: auto;
  }
}

.footer-info {
  text-align: center;
  font-family: Arial, Helvetica, sans-serif;
  display: flex;
  flex-direction: column;

  a,
  p {
    font-weight: 400;
    color: $font-primary;
  }

  a {
    text-decoration: none;
    margin: 20px;
  }
}
.flower-mobile {
  display: none;
}

.show-flower-mobile {
  display: block;
  position: absolute;
  right: 0;
  bottom: 0;
  transform: translateY(-112px);

  img {
    max-width: 100%;
    height: auto;
  }
}

.flower-desktop {
  display: none;
}

/* ----------------------*/
/* ----`*~ DESKTOP ~*´----*/
/* ----------------------*/

@media screen and (min-width: 1440px) {
  footer {
    min-height: 349px;
    justify-content: center;
  }

  .footer-dark-green,
  .footer-light-green {
    height: 500px;
    overflow: hidden;
  }

  .social-media-icons {
    gap: 70px;
    margin-bottom: 20px;

    img {
      width: 70px;
      height: auto;
    }
  }

  .footer-info {
    position: absolute;
    bottom: 20px;
  }

  a,
  p {
    font-size: 1.5rem;
  }

  .flower-mobile {
    display: none;
    overflow: hidden;
  }

  .flower-desktop {
    display: block;
    position: absolute;
    right: 0;
    bottom: 0;
    transform: translateY(31px);

    img {
      max-width: 100%;
      height: auto;
      display: block;
    }
  }
}
</style>
