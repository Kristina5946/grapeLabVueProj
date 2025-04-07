<template>
    <section class="tech-icons-section">
      <h2 class="section-title">Наш стек технологий</h2>
      <div class="icons-grid">
        <div 
          v-for="(icon, index) in icons" 
          :key="index" 
          class="icon-wrapper"
          @mouseenter="hoverIndex = index"
          @mouseleave="hoverIndex = -1"
        >
          <img 
            :src="icon.path" 
            :alt="'Технология ' + (index + 1)"
            class="tech-icon"
            :class="{ 'hovered': hoverIndex === index }"
          >
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const hoverIndex = ref(-1);
  
  const icons = [
    { path: '/icons/react.svg' },
    { path: '/icons/vue.svg' },
    { path: '/icons/angular.svg' },
    { path: '/icons/typescript.svg' },
    { path: '/icons/javascript.svg' },
    { path: '/icons/nodejs.svg' },
    { path: '/icons/nestjs.svg' },
    { path: '/icons/docker.svg' },
    { path: '/icons/kubernetes.svg' },
    { path: '/icons/postgresql.svg' },
    { path: '/icons/mongodb.svg' },
    { path: '/icons/redis.svg' },
    { path: '/icons/git.svg' },
    { path: '/icons/jenkins.svg' },
    { path: '/icons/aws.svg' },
    { path: '/icons/azure.svg' }
  ];
  </script>
  
  <style scoped src="../assets/styles/tech-stack.css"></style>