<template>
    <div class="main-container">
        <div v-for="(row, index) in rows" :key="index" class="row">
            <RowComponent :data="row"></RowComponent>
        </div>
    </div>
</template>

// MainComponent.vue
<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import RowComponent from '@/components/RowComponent.vue';

const rows = ref([]);
let intervalId;

// Generate random numbers for rows and items
function generateRandomData(rowsCount, itemsCount) {
  const data = [];
  for (let i = 0; i < rowsCount; i++) {
    const row = [];
    for (let j = 0; j < itemsCount; j++) {
      row.push(Math.floor(Math.random() * 100)); // Random number between 0 and 100
    }
    data.push(row);
  }
  return data;
}

// Function to update one random number in each row
function updateRandomNumber() {
  rows.value.forEach(row => {
    const index = Math.floor(Math.random() * row.length);
    row[index] = Math.floor(Math.random() * 100);
  });
}



const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      // Start or stop the interval based on whether the component is visible
      startRandomNumberUpdate();
    } else {
      stopRandomNumberUpdate();
    }
  });
});

function startRandomNumberUpdate() {
  intervalId = setInterval(updateRandomNumber, 1000);
}

function stopRandomNumberUpdate() {
  clearInterval(intervalId);
}

onMounted(() => {
  rows.value = generateRandomData(100, 40); // 5 rows, 20 items per row
  observer.observe(document.querySelector('.container'));
});

onUnmounted(() => {
  observer.disconnect();
});

</script>


<style scoped>
.main-container {
    padding: 10px;
    height: 100vh;
    width: 100%;
}

.row {
    display: flex;
    margin-bottom: 5px;
}

</style>