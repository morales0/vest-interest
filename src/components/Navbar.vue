<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { Icon } from '@iconify/vue';
import SelectNavLink from './SelectNavLink.vue';

import { ref } from 'vue'

const collapsed = ref(true)

const toggle = () => {
  collapsed.value = !(collapsed.value)
}

</script>

<template>
  <nav class="Navbar">
    <div class="logo">
      <img src="../assets/vest-interest-logo.png" alt="Vest Interest Logo" height="90">
    </div>
    <ul class="links main">
      <SelectNavLink name="School Program" :links="['Link1', 'Link 2']" />
      <li>
        <RouterLink to="/service-dogs">Service Dogs</RouterLink>
      </li>
      <li>
        <RouterLink to="/orgs">Organizations</RouterLink>
      </li>
    </ul>
    <ul class="links aside">
      <li>
        <RouterLink to="/about">About</RouterLink>
      </li>
      <li>
        <RouterLink to="/contact">Contact Us</RouterLink>
      </li>
      <li>
        <RouterLink to="/donate">Donate</RouterLink>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss">
.Navbar {
  display: flex;
  align-items: center;

  /* TODO: Make responsive container */
  width: 100%;
  padding: 1rem 2rem;

  /* use variable here */
  background-color: #283b68;
  color: white;
}

.logo {
  &>h3 {
    margin-bottom: .5rem;
  }
}

.links {
  display: flex;
  align-items: center;
  gap: 1rem;

  &>li {
    position: relative;
    list-style: none;
    font-size: 1.2rem;
  }

  &>li.select {
    display: flex;
    align-items: center;
    gap: .5rem;

    padding: .25rem .75rem;
    border: 1px solid rgb(80, 90, 113);
    border-radius: 3px;

    cursor: pointer;
  }

  & a {}
}

.links.aside {
  margin-left: auto;
}
</style>