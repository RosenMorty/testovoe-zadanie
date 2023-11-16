<template>
  <TheWrapper> 
    <div class="wrapper-container">
      <TheSearchbar />
      <div class="wrapper-divider" />
      <TheResult>
        <ItemPreview />
      </TheResult>
    </div>
  </TheWrapper>
</template>

<script setup>
import TheWrapper from './components/TheWrapper.vue';
import TheSearchbar from './components/TheSearchbar.vue';
import TheResult from './components/TheResult.vue'
import ItemPreview from './components/ItemPreview.vue';

</script>

<style scoped lang="scss">

.wrapper {
  &-container {
    display: flex;
    height: 575px;
    border-radius: 10px;
    background: #FDFDFD;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.10);
  }   
  &-divider {
    width: 1px;
    height: 100%;
    background-color: #E0E0E0;
  }
}
</style>
