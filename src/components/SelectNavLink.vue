<script setup lang="ts">
import { RouterLink } from 'vue-router'
import { Icon } from '@iconify/vue';
import { ref } from 'vue'

const props = defineProps(['name', 'links'])

const collapsed = ref(true)

const toggle = () => {
  collapsed.value = !(collapsed.value)
}
</script>

<template>
  <li class="select" @click="toggle">
    <div>{{ name }}</div>
    <Icon icon="ep:arrow-down-bold" width="20" class="select_toggle_icon" />
    <div v-if="collapsed" class="select_menu">
      <ul class="select_links">
        <li v-for="link in links" :key="link">
          <RouterLink to="#">{{ link }}</RouterLink>
        </li>
      </ul>
    </div>
  </li>
</template>

<style lang="scss">
.select_links {

  padding: 0;

  &>li {
    list-style: none;
  }
}

.select_menu {
  position: absolute;
  top: 50px;
  z-index: 100;

  min-width: 100%;

  background-color: #283b68;
  border: 1px solid rgb(156, 166, 189);
  border-radius: 3px;
  box-shadow: 0 0 5px 0 rgba(0, 0, 0, .2);
  padding: .5rem 2rem;
}
</style>