<template>
  <div className="chart-container">
    <Line :data="chartData" :options="chartOptions"/>
  </div>
</template>

<script setup>
import {ref} from 'vue';
import {Line} from 'vue-chartjs';
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  LineElement,
  PointElement,
  LinearScale,
  CategoryScale,
  Filler
} from 'chart.js';

ChartJS.register(
    Title,
    Tooltip,
    LineElement,
    PointElement,
    LinearScale,
    CategoryScale,
    Legend,
    Filler
);

const chartData = ref({
  labels: ['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс'],
  datasets: [
    {
      label: 'Верные ответы',
      borderColor: '#27AE60',
      backgroundColor: function(context) {
        const chart = context.chart;
        const {ctx, chartArea} = chart;
        if (!chartArea) {
          return null;
        }
        const gradient = ctx.createLinearGradient(0, chartArea.top, 0, chartArea.bottom);
        gradient.addColorStop(0, 'rgba(144, 238, 144, 0.4)');  // More opaque at the top
        gradient.addColorStop(0.5, 'rgba(144, 238, 144, 0.2)');  // More opaque at the top
        gradient.addColorStop(1, 'rgba(144, 238, 144, 0)');  // More transparent at the bottom
        return gradient;
      },
      pointStyle: "circles",
      pointRadius: 5,
      data: [20, 30, 50, 28, 50, 60, 40],
      fill: 'origin',
      tension: 0.4,
    },
    {
      label: 'Неверные ответы',
      borderColor: '#F39C12',
      backgroundColor: 'rgba(243, 156, 18, 0)',
      data: [27, 37, 70, 47, 70, 83, 60],
      fill: 'origin',
      tension: 0.4,
      pointStyle: "circles",
      pointRadius: 5,
    }
  ]
});

const chartOptions = ref({
  responsive: true,
  maintainAspectRatio: false,

  scales: {
    x: {
      grid: {
        display: false // This removes vertical grid lines
      },
      border: {
        display: false // This removes the x-axis line
      }
    },
    y: {
      beginAtZero: true,
      max: 100,
      ticks: {
        stepSize: 20, // This sets the step size to 20
        padding: 20
      },
      grid: {
        color: 'rgba(0, 0, 0, 0.1)',
        lineWidth: 1,
        drawBorder: false,
        drawTicks: false,
        borderDash: [5, 5]
      },
      border: {
        display: false // This removes the y-axis line
      }
    }
  },
  plugins: {
    legend: {
      align: 'end',
      labels: {
        padding: 20,
        usePointStyle: true,
        pointStyle: 'circle',
        font: {
          size: 14,
          opacity: 1,
        }
      }
    },
    filler: {
      propagate: true
    },
    tooltip: {
      callbacks: {
        label: function (context) {
          console.log(context.raw)
          return context.raw;
        },
        title: function() {
          return null; // Remove the title from the tooltip
        },
        afterBody: function() {
          return null; // Remove the additional information from the tooltip
        }
      },
      titleFont: {
        color: 'black' // Set the title font color to black
      },
      bodyFont: {
        size: 20,
        color: 'black' // Set the body font color to black
      },
      bodyColor: '#000',
      displayColors: false,
      backgroundColor: 'rgba(255, 255, 255, 1)', // Set the background color of the tooltip to white
      borderColor: 'rgba(0, 0, 0, .07)', // Set the border color of the tooltip to light grey
      borderWidth: 1, // Set the border width of the tooltip to 1px
      boxShadow: '2px 2px 10px 5px rgba(128, 128, 128, 0.8)' // Set the box shadow of the tooltip to light grey
    }
  }
});
</script>

<style scoped>
.chart-container {
  position: relative;
  height: 400px;
  width: 100%;
  min-width:300px;
}

</style>
