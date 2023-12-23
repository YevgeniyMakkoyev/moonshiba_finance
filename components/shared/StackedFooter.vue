<script setup lang="ts">
const FooterNavigationLinks = ref([
  // {
  //   name: 'GitHub',
  //   href: 'https://github.com/raised-network-foundation',
  //   icon: 'fa-brands fa-github',
  //   "animation-delay": 'delay-0',
  //   target: '_blank'
  // },
  {
    name: 'Twitter',
    href: 'https://twitter.com/moonshiba_fi',
    icon: 'fa-brands fa-twitter',
    "animation-delay": 'delay-100',
    target: '_blank'
  },
  // {
  //   name: 'Medium',
  //   href: 'https://blog.raised.network',
  //   icon: 'fa-brands fa-medium',
  //   "animation-delay": 'delay-200',
  //   target: '_blank'
  // },
  {
    name: 'Telegram',
    href: 'https://t.me/moon_shiba_official',
    icon: 'fa-brands fa-telegram',
    "animation-delay": 'delay-300',
    target: '_blank'
  },
  {
    name: 'Discord',
    href: 'https://discord.gg/7ae3ceE389',
    icon: 'fa-brands fa-discord',
    "animation-delay": 'delay-400',
    target: '_blank'
  },
]);

</script>

<template>
  <div class="py-4 px-6 flex justify-between">

    <div class="flex grow justify-center space-x-6">

      <!--      <img :src="DiscordSvg" class="h-8 w-8 text-white" style="color: green !important;" />-->

      <ULink v-for="link in FooterNavigationLinks" :to="link.href" :target="link.target">
        <i :class="`${link.icon} ${link['animation-delay']} transition text-xl text-gray-400 hover:text-gray-300 animate-pulse hover:animate-none duration-300`"></i>
      </ULink>
    </div>
  </div>
</template>

<style scoped>

</style>