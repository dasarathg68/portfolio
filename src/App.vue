<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavBar from '@/components/NavBar.vue'
import TheDrawer from '@/components/TheDrawer.vue'
import TheFooter from '@/components/TheFooter.vue'
</script>

<template>
  <div class="flex flex-col min-h-svh">
    <NavBar />
    <div class="flex-grow"></div>
    <RouterView />
    <div class="flex-grow"></div>
    <TheFooter />
  </div>
</template>

<style></style>
