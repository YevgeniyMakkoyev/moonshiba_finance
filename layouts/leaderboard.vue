<script setup lang="ts">
import StackedNavigation from "~/components/shared/StackedNavigation.vue";
import StackedFooter from "~/components/shared/StackedFooter.vue";
</script>

<template>
  <div class="mx-auto grow flex flex-col relative min-h-screen overflow-hidden">
    <div class="grow flex flex-col scroll-auto overflow-hidden">
      <StackedNavigation />
      <div class="grow p-8 max-w-7xl mx-auto">
        <slot />
      </div>
      <StackedFooter />
    </div>
  </div>
</template>

<style scoped>

</style>