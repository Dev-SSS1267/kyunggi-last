<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="absolute z-10 w-auto min-w-full min-h-full bg-black opacity-70">
  </div>
  <video class="object-cover absolute z-1 w-auto min-w-full min-h-full" autoplay muted loop id="intro">
    <source src="https://cdn.lunaiz.com/kghs/kyunggi_introduce.mp4" type="video/mp4">
  </video>
  <RouterView />
</template>
