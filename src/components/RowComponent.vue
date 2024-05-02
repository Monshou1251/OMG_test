<template>
    <div class="row">
        <div v-for="(item, index) in data" :key="index" class="item" @mouseover="startAnimation(index)"
            @mouseleave="stopAnimation(index)">
            {{ item }}
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

defineProps(['data'])

const rowData = ref([]);
const animations = [];

// Generate random numbers for items
function generateRandomData(itemsCount) {
    const data = [];
    for (let i = 0; i < itemsCount; i++) {
        data.push(Math.floor(Math.random() * 100)); // Random number between 0 and 100
    }
    return data;
}

// Start animation for a specific item
function startAnimation(index) {
    animations[index] = setInterval(() => {
        rowData.value[index] = Math.floor(Math.random() * 100); // Update the item with a new random number
    }, 1000);
}

// Stop animation for a specific item
function stopAnimation(index) {
    clearInterval(animations[index]);
}

// Initialize row data when component is mounted
onMounted(() => {
    rowData.value = generateRandomData(rowData.value.length);
});

</script>

<style scoped>
.row {
    display: flex;
}

.item {
    width: 40px;
    height: 40px;
    border: 1px solid black;
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 10px;
    cursor: pointer;
    transition: transform 0.1s ease-in-out;
}

.item:hover {
    transform: scale(0.8);
    background-color: #272727;
}
</style>