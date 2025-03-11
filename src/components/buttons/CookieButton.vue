<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  buttonText: string;
  buttonStyle: 'accept' | 'decline';
}>();
</script>

<template>
  <button :class="props.buttonStyle">
    {{ buttonText }}
  </button>
</template>

<style scoped lang="scss">
button {
  width: 142px;
  height: 48px;
  border-radius: 15px;
  border: 0;
  cursor: pointer;
  color: $font-primary;
  font-size: 1.25rem;
  font-weight: 900;
  text-align: center;
}

.accept {
  background-color: $bg-light-green;

  &:hover {
    background-color: $bg-yellow;
  }
}

.decline {
  background-color: $bg-purple;

  &:hover {
    background-color: $bg-red;
  }
}
</style>
