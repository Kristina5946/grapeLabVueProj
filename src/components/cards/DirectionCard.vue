<template>
  <div class="direction-card" :class="color">
    <div class="icon">
      <img :src="icon" alt="icon" />
    </div>
    <h3 class="title">{{ title }}</h3>
    <p class="description">{{ description }}</p>
    <div class="footer">
      <div class="rating">⭐ {{ rating }}</div>
      <div class="duration">⏱ {{ duration }}</div>
    </div>
  </div>

</template>

<script lang="ts" setup>
  defineProps<{
    title: string
    description: string
    icon: string
    rating: number
    duration: string
    color: string
  }>()
</script>

<style scoped>
.direction-card {
  border-radius: 16px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
  transition: transform 0.2s ease;
}
.direction-card.has-border {
  border: 1px solid #58427C;
}
.direction-card:hover {
  transform: translateY(-5px);
}
.icon {
  display: flex;
  justify-content: flex-end;
}
.icon img {
  width: 40px;
  height: 40px;
}
.title {
  font-weight: 600;
  font-size: 1.1rem;
  margin: 10px 0 5px;
}
.description {
  font-size: 0.95rem;
  line-height: 1.4;
}
.footer {
  display: flex;
  justify-content: space-between;
  font-size: 0.9rem;
  margin-top: 15px;
}

/* Цветовые стили */
.purple {
  background-color: #5c4080;
  color: white;
}
.white {
  background-color: white;
  color: #3c2a53;
  border: 1px solid #58427C;
}
.white .description {
  color: #555;
}
.white .footer {
  color: #777;
}
.purple .description {
  color: rgba(255, 255, 255, 0.8);
}
.purple .footer {
  color: rgba(255, 255, 255, 0.7);
}
</style>
