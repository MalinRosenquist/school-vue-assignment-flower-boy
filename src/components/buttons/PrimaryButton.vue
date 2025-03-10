<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  buttonText: string;
}>();
</script>

<template>
  <button class="primary-btn">
    {{ props.buttonText }}
  </button>
</template>

<style scoped lang="scss">
.primary-btn {
  width: 225px;
  height: 60px;
  border: solid 1px #000;
  border-radius: 15px;
  cursor: pointer;
  background-color: #000;
  color: $font-primary;
  font-size: 1.25rem;
  font-weight: 900;
  text-align: center;

  &:hover {
    background-color: $bg-yellow;
  }

  &:active {
    background-color: $bg-red;
  }
}

@media screen and (min-width: 1366px) {
  .primary-btn {
    width: 323px;
    height: 92px;
    font-size: 1.25rem;
    font-weight: 700;
  }
}
</style>
