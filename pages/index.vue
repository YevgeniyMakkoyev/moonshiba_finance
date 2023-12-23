<script setup lang="ts">

</script>

<template>
  <div class="absolute top-0 left-0 right-0 bottom-0 opacity-30 h-screen -z-10 overflow-hidden">
    <img id="bg_img" src="/background_hero.png" class="min-h-screen object-cover">
  </div>

  <div class="flex grow items-center">

    <div class="space-y-8">
      <div class="relative italic text-orange-400 font-bold inline-flex flex-col">
        <div>
          <span class="uppercase text-2xl sm:text-4xl md:text-4xl lg:text-5xl">Building for</span> <span class="uppercase text-2xl sm:text-4xl md:text-3xl md:hidden">community</span>
        </div>
        <div>
          <span class="text-orange-50 uppercase italic text-2xl sm:text-4xl md:text-4xl lg:text-5xl">with help of</span> <span class="text-orange-50 uppercase italic text-2xl sm:text-4xl md:text-3xl md:hidden">community</span>
        </div>

        <span class="absolute -right-5 translate-x-full md:h-full md:flex md:items-center hidden md:block md:text-7xl lg:text-8xl uppercase">
          Community
        </span>
      </div>

      <div class="font-light text-lg md:text-2xl">
<!--        Raised Network approach to development is simple yet powerful: we strongly emphasize the importance of the community and its involvement. <br /> We believe that the community is the most important asset and we want to build a strong and healthy community around Raised Network.-->
<!--        <br />-->
<!--        <br />-->
<!--        The approach we choose to follow is simple yet powerful: we strongly emphasize the importance of the community and its involvement in the development. <br /> We believe that the community is the most important asset and we want to build a strong and healthy community around Raised Network.-->
<!--        <br />-->
<!--        <br />-->
        The community driven approach fits perfectly within Raised Network's vision and mission. <br />
        We want to build a strong and healthy community, providing tools and services that will benefit the community and the whole ecosystem.
      </div>

      <div class="flex justify-center">
        <ULink to="/deploy/solana" class="bg-orange-400 hover:bg-orange-500 duration-300 text-gray-900 font-bold py-2 px-4 rounded-full uppercase">
          Our application
        </ULink>
      </div>
    </div>
  </div>

<!--  <div class="h-[500px]">-->
<!--    <div>-->
<!--      <div class="text-xl sm:text-2xl md:text-3xl sm:text-2xl md:text-3xl text-orange-50">-->
<!--        <p>Here you can find all services:</p>-->

<!--        <div class="mt-4">-->
<!--          <ULink v-for="feature in FeaturesNavigation" :to="feature.href" :target="feature.target" class="text-orange-50">-->
<!--            {{ feature.name }}-->
<!--          </ULink>-->
<!--        </div>-->
<!--      </div>-->
<!--    </div>-->
<!--  </div>-->
</template>

<style scoped>
@keyframes colorChange {
  0% {
    color: black;
  }
  100% {
    color: green;
  }
}

.letter-animation {
  display: inline-block;
}

.letter-animation span {
  display: inline-block;
  opacity: 0;
  animation: colorChange 1s forwards;
}

.letter-animation span:nth-child(1) {
  animation-delay: 0.1s;
}

.letter-animation span:nth-child(2) {
  animation-delay: 0.2s;
}

.letter-animation span:nth-child(3) {
  animation-delay: 0.3s;
}
</style>