<template>
  <div class="circular-progress">
    <svg :width="size" :height="size" viewBox="0 0 36 36" class="circular-chart">
      <path
          class="circle-bg"
          :style="{ strokeWidth: lineWidth }"
          d="M18 2.0845
           a 15.9155 15.9155 0 0 1 0 31.831
           a 15.9155 15.9155 0 0 1 0 -31.831"
      />
      <path
          class="circle"
          :style="{ 'stroke-dasharray': progress + ', 100', transition: 'stroke-dasharray 1s ease-out', strokeWidth: lineWidth, stroke: lineColor }"
          d="M18 2.0845
           a 15.9155 15.9155 0 0 1 0 31.831
           a 15.9155 15.9155 0 0 1 0 -31.831"
      />
    </svg>
    <span class="percentage" :style="[`color:${lineColor}`, `font-size:${perSize}px`]">{{ percentage }}%</span>
  </div>
</template>

<script setup>
import { ref, onMounted, computed } from 'vue';

const props = defineProps({
  percentage: {
    type: Number,
    required: true
  },
  size: {
    type: Number,
    default: 100
  },
  perSize: {
    type: Number,
    default: 20
  },
  lineWidth: {
    type: Number,
    default: 3
  },
  lineColor: {
    type: String,
    default: '#ffa500'
  }
});

const progress = ref(0);

const progressPercentage = computed(() => (props.percentage / 100) * 100);

onMounted(() => {
  setTimeout(() => {
    progress.value = progressPercentage.value;
  }, 100); // небольшой таймаут для запуска анимации
});
</script>

<style>
.circular-progress{
  display:flex;
  align-items: center;
  justify-content: center;
}
.circular-chart {
  display: block;
  margin: 0 auto;
  max-height: 250px;
}

.circle-bg {
  fill: none;
  stroke: #eee;
}

.circle {
  fill: none;
  stroke-linecap: round;
}

.percentage {
  position: absolute;
  font-family: "Golos Text", sans-serif;
  font-weight: 700;
  text-anchor: middle;
}
</style>
