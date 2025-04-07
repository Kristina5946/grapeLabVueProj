<template>
    <section class="process-section">
      <h2 class="section-title">Процесс разработки</h2>
      <div class="process-line"></div>
      <div class="process-container">
        <div
          v-for="(step, index) in steps"
          :key="index"
          class="process-step"
          :style="{ '--order': index }"
        >
          <div class="step-icon-container">
            <img :src="step.img" alt="icon" class="step-icon" />
          </div>
          <div class="step-content">
            <h3 class="step-title">{{ step.title }}</h3>
            <p class="step-description">{{ step.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  const steps = [
    {
      title: "Аналитический воркшоп",
      description: "На этом этапе мы изучаем ваш бизнес, цели, проблемы и приоритеты. В ходе нескольких сессий мозгового штурма мы анализируем текущие рабочие процессы и определяем направления для будущего развития.",
      img: "/icons/analysis.svg"
    },
    {
      title: "Проектирование",
      description: "На этом этапе, после сбора ваших требований в ходе сессии на whiteboard, мы приступаем к разработке концепции, созданию прототипов и тестированию пользовательского опыта вашего продукта или платформы.",
      img: "/icons/design.svg"
    },
    {
      title: "Разработка",
      description: "На этом этапе ведётся программирование и кодирование на основе утверждённых вами дизайнов. Наш цикл разработки включает три этапа: Alpha, Beta и Release.",
      img: "/icons/development.svg"
    },
    {
      title: "Тестирование",
      description: "Мы продолжаем процесс валидации на основе данных, проводим тщательное QA-тестирование для каждого релиза вашего продукта , чтобы гарантировать, что финальная версия готова к выходу на рынок.",
      img: "/icons/testing.svg"
    },
    {
      title: "Запуск и поддержка",
      description: "На этом этапе ваш продукт  выходит в продакшн. После вашего одобрения наши разработчики развёртывают его в рабочей среде. Мы полностью берём на себя управление облачным и локальным хостингом.",
      img: "/icons/deploy.svg"
    },
    {
        title: "Обслуживание",
        description: "Для обеспечения непрерывного совершенствования мы выполняем постоянное обслуживание продукта, внедряем рыночные стратегии и предоставляем оперативную поддержку и исправление ошибок.",
        img: "/icons/deploy.svg"
    }
  ];
  </script>
  
  <style lang="css" src="../assets/styles/process.css" />
  