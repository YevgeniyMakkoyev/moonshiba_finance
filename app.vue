<template>
  <div class="flex">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
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
  box-shadow: inset 50px 50px 150px 250px rgba(0,0,0,.2);

}



</style>

<script setup lang="ts">
import '~/assets/css/font-awesome/all.min.css';

useHead({
  title: 'MoonShiba.finance - Official Website',
  meta: [
    { name: 'description', content: 'The best memecoin on solana!'}
  ],
})
</script>