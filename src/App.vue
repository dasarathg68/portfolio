<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavBar from '@/components/NavBar.vue'
import { ref } from 'vue'
import TheDrawer from '@/components/TheDrawer.vue'
import TheFooter from '@/components/TheFooter.vue'
import { themes } from '@/utils/themes'

const themesAvailable = ref(themes.themes)
const currentTheme = ref('cyberpunk')
</script>

<template>
  <div class="flex flex-col min-h-svh" :data-theme="currentTheme">
    <NavBar
      :themesAvailable="themesAvailable"
      @theme-changed="(newTheme) => (currentTheme = newTheme)"
    />
    <div class="flex-grow"></div>
    <RouterView />
    <div class="flex-grow"></div>
    <TheFooter />
  </div>
</template>

<style></style>
