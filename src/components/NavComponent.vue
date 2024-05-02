<template>
  <div class="nav-container">
    <div class="logo">
        OMG...TEST
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.nav-container {
    height: 100%;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    border-bottom: dashed 1px var(--color-border);
}

.logo {
    margin-left: 20px;
    width: 120px;
    font-size: 18px;
    font-weight: 800;
    background-image: linear-gradient(to right, #4793AF, #dd5846, #FFC470, #8B322C);
    background-clip: text;
    color: transparent; 
}

</style>