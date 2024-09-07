<script setup lang="ts">
import LandTop from './components/LandTop.vue'
import LandMain from './components/LandMain.vue';
</script>

<template>
 <div class="flex justify-center flex-col p-20">
 <LandTop></LandTop>
 <LandMain></LandMain>
 </div>   
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
