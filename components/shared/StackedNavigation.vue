<script setup lang="ts">
const NavigationItems = ref([
  {
    name: 'Home',
    href: '/',
    target: '_self',
    disabled: false
  },
  {
    name: 'Roadmap (coming soon)',
    href: 'https://whitepaper.moonshiba.finance/',
    target: '_blank',
    disabled: true
  },
  {
    name: 'Crafting',
    href: '/',
    target: '_self',
    disabled: true
  },
]);
</script>

<template>
  <div class="py-4 px-6 flex justify-between">
    <div class="flex space-x-4">
      <img src="/official-logo.png" class="h-8 w-8" />
    </div>
    <div class="space-x-2 items-center flex">
      <ULink v-for="item in NavigationItems" :key="item.name" :to="item.href" :disabled="item.disabled" :class="{'text-gray-400 cursor-not-allowed': item.disabled}" class="uppercase text-xs text-gray-200 font-light" :target="item.target">
        {{ item.name }}
      </ULink>
    </div>
  </div>
</template>

<style scoped>

</style>