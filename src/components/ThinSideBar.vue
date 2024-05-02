<template>
  <div class="thinsidebar-container">
    <a href="https://github.com" class="icon-link">
      <svg-icon type="mdi" :path="mdiGithub"></svg-icon>
    </a>
    <a href="https://www.google.com" class="icon-link">
      <svg-icon type="mdi" :path="mdiGoogle"></svg-icon>
    </a>
    <a href="https://www.linkedin.com" class="icon-link">
      <svg-icon type="mdi" :path="mdiLinkedin"></svg-icon>
    </a>
  </div>
</template>

<script setup>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiGithub, mdiGoogle, mdiLinkedin } from '@mdi/js';
</script>

<style scoped>
.thinsidebar-container {
  border-left: dashed 1px var(--color-border);
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding-bottom: 10px;
  gap: 10px;
}

.icon-link {
  color: inherit; 
  text-decoration: none; 
}
</style>
