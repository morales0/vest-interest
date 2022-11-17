<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <header>
    <Navbar />
  </header>

  <main>
    <RouterView />
  </main>

  <footer>
    Footer
  </footer>
</template>

<style scoped>
header {}

main {
  flex: 1 0 auto;
  border: 1px solid white;
  padding: .5rem;
}

footer {
  border: 1px solid white;
  padding: .5rem;
}
</style>
