<script setup lang="ts">
import { RouterLink } from 'vue-router'

</script>

<template>
  <nav class="Navbar">
    New Nav
    <ul>
      <li>
        <RouterLink to="/about">About</RouterLink>
      </li>
    </ul>
  </nav>
</template>

<style>
.Navbar {
  background-color: pink;
  color: black;
}
</style>