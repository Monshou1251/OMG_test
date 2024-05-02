<template>
    <div class="footer-container">
        <div class="logo">
            {{ currentDate }}
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const currentDate = ref('');

onMounted(() => {
    const date = new Date();
    const options = { year: 'numeric', month: 'long', day: 'numeric' };
    currentDate.value = date.toLocaleDateString('en-US', options);
});
</script>

<style scoped>
.footer-container {
    border-top: dashed 1px var(--color-border);
    height: 100%;
    width: auto;
    display: flex;
    align-items: center;
    justify-content: flex-end;
}

.logo {
    margin-right: 5px;
    width: 90px;
    font-size: 14px;
    font-weight: 600;
    background-image: linear-gradient(to right, #4793AF, #dd5846, #FFC470, #8B322C);
    background-clip: text;
    color: transparent; 
}
</style>