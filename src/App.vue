<script setup lang="ts">
import About from './components/About.vue';
import Header from './components/Header.vue';
import Projects from './components/Projects.vue';
import Footer from './components/Footer.vue';
import Timeline from './components/Timeline.vue';
</script>

<template>
  <div class="app">
    <Header />
    <main>
      <About />
      <Projects />
      <Timeline />
    </main>
    <Footer />
  </div>
</template>

<style>
.app {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 6rem;
  padding: 6rem 0;
}

.app>* {
  width: 100%;
}
</style>
