<template>
  <div class="container">
    <nav class="navbar"> 
      <NavComponent></NavComponent>
    </nav>
    <main class="main">
      <MainComponent></MainComponent>
    </main>
    <aside class="sidebar">
      <SideBar></SideBar>
    </aside>
    <aside class="thinsidebar">
      <ThinSideBar></ThinSideBar>
    </aside>
    <footer class="footer">
      <FooterComponent></FooterComponent>
    </footer>
  </div>
</template>

<script setup>
import NavComponent from '@/components/NavComponent.vue';
import MainComponent from '@/components/MainComponent.vue';
import SideBar from '@/components/SideBar.vue';
import ThinSideBar from '@/components/ThinSideBar.vue';
import FooterComponent from '@/components/FooterComponent.vue';

</script>

<style scoped>
.container {
  max-height: 100vh;
  height: 100vh; 
  width: 100%; 
  display: grid;
  grid-template-columns: 60px auto 40px;
  grid-template-rows: 50px auto 40px;
  grid-template-areas: 
    "navbar navbar navbar"
    "sidebar main thinsidebar"
    "footer footer footer";
}

.main {
  grid-area: main;
  overflow-y: auto; 
  max-height: calc(100vh - 90px);
}

.sidebar {
  grid-area: sidebar;
}

.thinsidebar {
  grid-area: thinsidebar;
}

.footer {
  grid-area: footer;
}

.navbar {
  grid-area: navbar;
}


</style>

