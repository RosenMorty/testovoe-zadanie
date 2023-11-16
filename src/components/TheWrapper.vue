<template>
  <div class="the-wrapper">
    <TheToolbar />
    <slot />
  </div>
</template>

<script setup>
import TheToolbar from './TheToolbar.vue';
</script>

<style scoped lang="scss">
.the-wrapper {
  margin: 0 50px 0 50px;
}
</style>