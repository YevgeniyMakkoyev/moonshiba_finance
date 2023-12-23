<template>
<!--  <div class="flex">-->
<!--    <NuxtLayout>-->
<!--      <NuxtPage />-->
<!--    </NuxtLayout>-->
<!--  </div>-->

  <div class="bg-gray-800 h-screen flex items-center">
    <h1 class="text-4xl text-center font-bold py-8 flex justify-center flex-1 text-orange-400">
      MoonShiba Finance - Coming Soon
    </h1>
  </div>
</template>

<style>
@font-face {
  font-family: 'Proto Mono Light';
  font-display: optional;
  src: url('/public/fonts/Proto Mono Light.ttf') format('ttf');
}

body {
  @apply antialiased font-sans text-gray-200 bg-gray-900;
  font-family: "Proto Mono Light", monospace;
  font-size: 0.8rem;
}
</style>

<script setup lang="ts">
import '~/assets/css/font-awesome/all.min.css';
</script>