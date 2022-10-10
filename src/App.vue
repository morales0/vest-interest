<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <nav>
      Navbar
    </nav>
  </header>

  <main>
    <RouterView />
  </main>

  <footer>
    Footer
  </footer>
</template>

<style scoped>
header {
  border: 1px solid white;
  padding: .5rem;
}

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
