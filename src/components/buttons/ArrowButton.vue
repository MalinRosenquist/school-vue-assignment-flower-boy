<script setup lang="ts"></script>

<template>
  <button class="svg-arrow-btn">
    <svg width="71" height="39" viewBox="0 0 71 39" fill="none" xmlns="http://www.w3.org/2000/svg">
      <line x1="1.06066" y1="1.93934" x2="34.0607" y2="34.9393" stroke="white" stroke-width="3" />
      <line x1="69.0607" y1="2.06066" x2="34.0607" y2="37.0607" stroke="white" stroke-width="3" />
    </svg>
  </button>
</template>

<style scoped lang="scss">
.svg-arrow-btn {
  background: transparent;
  border: 0;

  svg {
    width: 68px;
    height: 35px;
    border: 0;
    cursor: pointer;
  }

  &:hover svg line {
    stroke: $bg-yellow;
  }

  &:active svg line {
    stroke: $bg-red;
  }
}
</style>
