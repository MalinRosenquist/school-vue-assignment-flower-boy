<script setup lang="ts">
import { ref } from 'vue';
import CookieButton from '../buttons/CookieButton.vue';

const showCookieBar = ref(true);

function handleAccept() {
  showCookieBar.value = false;
}

function handleDecline() {
  showCookieBar.value = false;
}
</script>

<template>
  <section v-if="showCookieBar" class="cookie-bar">
    <p class="cookie-bar-text">Do you want to allow cookies for a better experience?</p>
    <img
      class="img-cookie-bar"
      src="@/assets/bee.svg"
      alt="An illustration of a bee, with its characteristic black and yellow stripes and wings."
      height="114px"
      width="83px"
    />
    <div class="cookie-bar-buttons">
      <CookieButton @click="handleAccept" buttonText="Accept" buttonStyle="accept" />
      <CookieButton @click="handleDecline" buttonText="Decline" buttonStyle="decline" />
    </div>
  </section>
</template>

<style scope lang="scss">
.cookie-bar {
  border-radius: 15px;
  background-color: $bg-light-blue;
  width: 91.9%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  position: fixed;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 15px;
  text-align: center;
  padding: 60px 10px;
  z-index: 2;

  .cookie-bar-text {
    font-size: 1.25rem;
    font-weight: 900;
    margin: 0;
    text-wrap: balance;
  }
}

.img-cookie-bar {
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
  margin-bottom: 20px;
}

.cookie-bar-buttons {
  display: flex;
  gap: 10px;
}

/* ----------------------*/
/* ----`*~ DESKTOP ~*´----*/
/* ----------------------*/

@media screen and (min-width: 1366px) {
  .cookie-bar {
    border: 4px solid #000;
    height: 179px;
    width: 80.97%;
    z-index: 10;
    flex-direction: row;
    justify-content: left;
    padding: 32px;
    top: unset;
    left: 50%;
    transform: translate(-50%);
    bottom: 0;

    .img-cookie-bar {
      order: 1;
      margin-bottom: 0;
    }

    .cookie-bar-text {
      order: 2;
      padding-left: 15px;
    }

    .cookie-bar-buttons {
      order: 3;
      flex-grow: 1;
      justify-content: end;
    }
  }
}
</style>
