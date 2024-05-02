<template>
  <div class="app-container">
    <RouterView />
  </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
</script>


<style>

.app-container {
  height: 100%;
  width: 100%;
}

::-webkit-scrollbar {
    width: 10px; 
    height: 10px; 
}

::-webkit-scrollbar-thumb {
     
    border-radius: 12px;
    background: #555555bd; 
}

::-webkit-scrollbar-thumb:hover {
  background: #888; 
    cursor: pointer;
}


::-webkit-scrollbar-track {
    background: var(--color-background); 
    border: solid 1px #55555544;
    border-radius: 12px;
}

::-webkit-scrollbar-corner {
  background: rgba(0,0,0,0);
}

</style>
