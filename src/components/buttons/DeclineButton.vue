<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  buttonText: string;
}>();
</script>

<template>
  <button class="decline-btn">
    {{ props.buttonText }}
  </button>
</template>

<style scoped lang="scss">
.decline-btn {
  width: 142px;
  height: 48px;
  border-radius: 15px;
  border: 0;
  cursor: pointer;
  background-color: $bg-purple;
  color: $font-primary;
  font-size: 1.25rem;
  font-weight: 900;
  text-align: center;

  &:hover {
    background-color: $bg-yellow;
  }
}
</style>
