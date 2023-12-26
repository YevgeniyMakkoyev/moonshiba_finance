<script setup lang="ts">
import StackedNavigation from "~/components/shared/StackedNavigation.vue";
import StackedFooter from "~/components/shared/StackedFooter.vue";
</script>

<template>
  <div id="a_test" class="mx-auto grow flex flex-col relative min-h-screen">
    <div class="grow flex flex-col">
      <StackedNavigation />
      <div class="grow p-8 max-w-7xl mx-auto overflow-scroll-y">
        <slot />
      </div>
      <StackedFooter />
    </div>
  </div>
</template>

<style scoped>

</style>