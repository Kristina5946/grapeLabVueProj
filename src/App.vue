<template>
  <div class="app">
    <Direction />
    <DevelopmentProcess />
    <TechStack />
  </div>
</template>

<script setup lang="ts">
  //@ts-ignore
  import DevelopmentProcess from './components/DevelopmentProcess.vue'
  //@ts-ignore
  import Direction from './components/Direction.vue'
  //@ts-ignore
  import TechStack from './components/TechStack.vue'
</script>

<style scoped>
  .app {
    padding: 5% 10%; /* Отступы 10% по бокам */
    background-color: #F2F0F5;
    min-height: 100vh;
  }
</style>


