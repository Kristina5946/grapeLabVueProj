
<script lang="ts">
    import DirectionCard from './cards/DirectionCard.vue'

    const directions = [
    {
        title: 'Мобильные приложения',
        description: 'Разработка нативных и кроссплатформенных решений для iOS и Android.',
        icon: '/icons/mobile.svg',
        rating: 4.8,
        duration: '30д',
        color: 'purple'
    },
    {
        title: 'WEB разработка',
        description: 'Создание адаптивных сайтов и веб-приложений для любых устройств.',
        icon: '/icons/web.svg',
        rating: 4.8,
        duration: '30д',
        color: 'purple'
    },
    {
        title: 'QA и тестирование',
        description: 'Обеспечение качества и тестирование программных решений.',
        icon: '/icons/qa.svg',
        rating: 4.8,
        duration: '30д',
        color: 'white'
    },
    {
        title: 'UI/UX-дизайн',
        description: 'Проектирование и создание удобных и эстетичных интерфейсов.',
        icon: '/icons/uiux.svg',
        rating: 4.8,
        duration: '30д',
        color: 'white'
    },
    {
        title: 'Десктопные решения',
        description: 'Разработка под Windows, macOS и Linux. Индивидуальные решения под ваши задачи.',
        icon: '/icons/desktop.svg',
        rating: 4.8,
        duration: '30д',
        color: 'purple'
    },
    {
        title: 'Проектирование ПО',
        description: 'Создание архитектуры и проектирование программных решений.',
        icon: '/icons/architecture.svg',
        rating: 4.8,
        duration: '30д',
        color: 'white'
    },
    {
        title: 'Интернет вещей (IoT)',
        description: 'Разработка нативных и кроссплатформенных приложений.',
        icon: '/icons/iot.svg',
        rating: 4.8,
        duration: '30д',
        color: 'purple'
    },
    {
        title: 'Исследования (R&D)',
        description: 'Проведение исследований и разработка инновационных решений.',
        icon: '/icons/research.svg',
        rating: 4.8,
        duration: '30д',
        color: 'white'
    }
    ]

    export default {
        components: {
            DirectionCard
        },
        data() {
            return {
                directions
            }
        }
    }
</script>


<template>
    <h1 class="page-title">Направления разработки</h1>
        <div class="cards-grid">
        <!-- Первые две квадратные карточки (2x1) -->
        <DirectionCard class="card-square" v-bind="directions[0]" />
        <DirectionCard class="card-square" v-bind="directions[1]" />
        
        <!-- Вертикальные карточки (1x2) -->
        <DirectionCard class="card-vertical" v-bind="directions[2]" />
        <DirectionCard class="card-vertical" v-bind="directions[3]" />
        
        <!-- Горизонтальная карточка во второй строке (2x1) -->
        <DirectionCard class="card-horizontal" v-bind="directions[4]" />
        
        <!-- Последний ряд -->
        <DirectionCard class="card-horizontal" v-bind="directions[5]" />
        <DirectionCard class="card-square" v-bind="directions[6]" />
        <DirectionCard class="card-square" v-bind="directions[7]" />
        </div>
</template>

<style scoped src="../assets/styles/cards.css" />
