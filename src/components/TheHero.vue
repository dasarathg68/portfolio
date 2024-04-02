<template>
  <div class="hero min-h-svh w-full" :style="{ backgroundImage: `url(${imgSrc})` }">
    <div class="hero-overlay bg-opacity-60"></div>
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <h1 class="mb-5 text-5xl font-bold">Hello there</h1>
        <p class="mb-5">
          Providing top notch services to startups, industries and agencies to realize their product
          vision and development workflow
        </p>
        <button class="btn btn-primary">View Profile</button>
      </div>
    </div>
  </div>
</template>
<script setup>
import img from '../assets/images/artmaybe.jpg'
import { ref } from 'vue'
const imgSrc = ref(img)
</script>
