<script setup lang="ts">

</script>

<template>

  <div class="absolute top-0 left-0 right-0 bottom-0 opacity-30 h-screen -z-10 overflow-hidden border-b-2 border-gray-50">
    <video id="bg_img" src="/background_hero_animation.mp4" autoplay loop class="min-h-screen object-cover" />
  </div>

  <div class="flex grow items-center min-h-screen">

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
        <div>
          The community driven approach fits perfectly within <span class="text-orange-400">$MSHIBA</span> vision and mission. <br />
          We want to build a strong and healthy community, providing tools and services that will benefit the community and the whole ecosystem.
        </div>
      </div>

      <div class="flex flex-col md:flex-row justify-center">
        <ULink to="https://forms.gle/aUViMBudqZjs7o8k6" target="_blank" class="bg-gray-600/50 hover:bg-gray-600 duration-300 text-gray-50 font-bold py-2 px-4 uppercase md:rounded-l-full rounded-l-none">
          <img src="https://www.gstatic.com/images/branding/product/1x/forms_2020q4_48dp.png" class="mx-4 md:px-0 h-6 w-6 inline-block" />
          Feedback form
        </ULink>
        <ULink to="https://raydium.io/swap/?inputCurrency=sol&outputCurrency=4NmXYNGCwMC3DSvvt7o8ULfEx8rJ9w7QdPVrq3kcMVem&inputAmount=5.368571556&outputAmount=207906.203195&fixed=in" target="_blank" class="bg-gray-600/50 hover:bg-gray-600 duration-300 text-gray-50 font-bold py-2 px-4 uppercase">

          <img src="https://raydium.io/favicon.ico" class="mx-4 md:px-0 h-6 w-6 inline-block" />
          Raydium
        </ULink>
        <ULink to="https://rugcheck.xyz/tokens/4NmXYNGCwMC3DSvvt7o8ULfEx8rJ9w7QdPVrq3kcMVem" target="_blank" class="bg-gray-600/50 hover:bg-gray-600 duration-300 text-gray-50 font-bold py-2 px-4 uppercase">
          <img src="https://rugcheck.xyz/favicon.png" class="mx-4 md:px-0 h-6 w-6 inline-block" />
          RugCheck
        </ULink>
        <ULink to="https://birdeye.so/token/4NmXYNGCwMC3DSvvt7o8ULfEx8rJ9w7QdPVrq3kcMVem?chain=solana" target="_blank" class="bg-gray-600/50 hover:bg-gray-600 duration-300 text-gray-50 font-bold py-2 px-4 uppercase md:rounded-r-full rounded-r-none">
          <img src="https://birdeye.so/favicon.ico" class="mx-4 md:px-0 h-6 w-6 inline-block" />
          Birdeye
        </ULink>
      </div>
    </div>
  </div>


  <section id="advantages" class="min-h-screen space-y-4 items-center flex">
    <div class="space-y-8">
      <h1 class="text-4xl uppercase font-bold text-orange-400">Upcoming Features</h1>

      <div class="text-sm">
        <p>We strongly believe that a meme token should be always backed by a committed community, and concrete utility.</p>
        <p>That's why we are working hard to provide the community with the best tools and services over the Solana ecosystem.</p>

        <p>What is coming next? Well, we are working on a lot of things, but it will be always the community to decide what to build next.</p>
      </div>


      <div class="flex flex-wrap">
        <div class="w-full md:w-1/2 cursor-pointer">
          <div class="m-4 p-4 bg-gray-800/50 space-y-4 rounded-md hover:bg-gray-800/70 duration-300 hover:shadow-xl">
            <h1 class="text-2xl text-orange-400">Zealy Telegram Bot</h1>
            <p>Zealy is the ultimate platform for community engagement. It lets founders show their appreciation to their loyal community members with awesome rewards. However, Zealy only works with discord, so we need a different solution for our telegram community. That's why we are developing our own bot that will integrate with Zealy and offer the same features to our telegram users. This bot will also be available to other communities who want to use Zealy on telegram, but don't have the resources to create their own bot. The only requirement is to burn a small amount of MSHIB tokens to access the bot.
            </p>
          </div>
        </div>
        <div class="w-full md:w-1/2 cursor-pointer">
          <div class="m-4 p-4 bg-gray-800/50 space-y-4 rounded-md hover:bg-gray-800/70 duration-300 hover:shadow-xl">
            <h1 class="text-2xl text-orange-400">Liquidity Tracker</h1>
            <p>Liquidity Tracker is an essential tool for every degen investor. Since our community is also degen, we aim to provide this useful tool to give investors insights on the new liquidity added recently with aggregation and verification in real time. This way, we provide users with an easy-to-use and helpful tool to be independent. We will also provide a free space for members to discuss third-party coins, in order to create an inclusive and collaborative community with other projects.
            </p>
          </div>
        </div>
        <div class="w-full md:w-1/2 cursor-pointer">
          <div class="m-4 p-4 bg-gray-800/50 space-y-4 rounded-md hover:bg-gray-800/70 duration-300 hover:shadow-xl">
            <h1 class="text-2xl text-orange-400">Snipe Bot</h1>
            <p>The Snipe bot is a powerful and convenient tool that allows our members to buy coins directly from telegram, without having to switch to other platforms or apps. It also lets them manage their positions securely and independently, with features such as stop-loss, take-profit, and trailing-stop. The Snipe bot is integrated with the most popular and reliable exchanges, such as Raydium, Orca, and FluxBeam. The Snipe bot is easy to use, fast, and reliable, and it can help you snipe the best deals in the crypto market.
            </p>
          </div>
        </div>
        <div class="w-full md:w-1/2 cursor-pointer">
          <div class="m-4 p-4 bg-gray-800/50 space-y-4 rounded-md hover:bg-gray-800/70 duration-300 hover:shadow-xl">
            <h1 class="text-2xl text-orange-400">Governance platform</h1>
            <p>Welcome to the Governance Platform, a dynamic space where the MSHIBA community actively participates in shaping the future of our project. At MSHIBA, we believe in decentralization, transparency, and community-driven decision-making. This platform serves as a hub for all MSHIBA token holders to exercise their voting rights and influence the direction of the project.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

@keyframes matrix-move {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(100%);
  }
}

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