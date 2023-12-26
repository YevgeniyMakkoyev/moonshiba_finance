<script setup lang="ts">
definePageMeta({
  layout: 'leaderboard',
})

const leaderboardColumns = ref<any[]>([
  {
    key: 'rank',
    label: 'Rank',
    sortable: true,
  },
  {
    key: 'profile',
    label: 'User profile',
    sortable: true,
  },
  {
    key: 'xp',
    label: 'XP earned',
    sortable: true,
  },
  {
    key: 'quests',
    label: 'Quests completed',
    sortable: true,
  },
]);
const leaderboard = ref<any[]>([]);
const page = ref(1)
const pageCount = 5

const rows = computed(() => {
  return leaderboard.value.slice((page.value - 1) * pageCount, (page.value) * pageCount)
})


const accordionItems = ref<any[]>([{
  label: 'Getting Started',
  icon: 'i-heroicons-information-circle',
  defaultOpen: true,
  content: 'By completing quests, you will earn XP and level up your profile. The higher your level, the more rewards you will receive. You can also earn XP by contributing to the community through our Telegram bot (coming soon).'
}, {
  label: 'Contributing',
  icon: 'i-heroicons-eye-dropper',
  content: 'Contributing and being active in the Telegram community will earn you XP. The bot will track your activity and reward you accordingly. The more active you are, the more XP you will earn. (coming soon)'
}]);


onMounted(async () => {

  // Make request to API https://api.zealy.io/communities/:subdomain/leaderboard
  // Add header x-api-key from constants.ts
  // query with limit and page
  // https://api.zealy.io/communities/:subdomain/users

  const response = [
    {
      "userId": "3f8f4509-ea45-45d7-9e40-89c6dd3b9be3",
      "xp": 12,
      "name": "BradPete",
      "avatar": "https://zealy-webapp-images-prod.s3.eu-west-1.amazonaws.com/public/3f8f4509-ea45-45d7-9e40-89c6dd3b9be3-social-davatar.jpg",
      "numberOfQuests": 4,
      "addresses": {},
      "address": "4Kif649Pe7S6WPE8TdyjiJQBB7JXVzcy1tUxWxtoVpd9",
      "twitterId": "1222560887828910080",
      "discord": "_xrpedro",
      "twitter": "_XRPedro",
      "discordId": "883353815993176124",
      "connectedWallet": "0x27337878B161C04Bd0b2D99a12ddE85b31F9265f"
    },
    {
      "userId": "411d7a3b-226d-4495-a59a-c14805053f6f",
      "xp": 12,
      "name": "Flikzee",
      "avatar": "https://zealy-webapp-images-prod.s3.eu-west-1.amazonaws.com/public/411d7a3b-226d-4495-a59a-c14805053f6f-logo.png",
      "numberOfQuests": 4,
      "addresses": {},
      "address": "FMVebQEr34hrf8L3f1hMEwbzMPWuQzFWphYz6CV3bJ15",
      "twitterId": "1457211288141008900",
      "discord": "tyongtas",
      "twitter": "gunngz",
      "discordId": "870144116623822888",
      "connectedWallet": ""
    },
    {
      "userId": "69d82a94-a411-4b01-950c-cdaafd05200d",
      "xp": 12,
      "name": "vinceandrei",
      "avatar": null,
      "numberOfQuests": 4,
      "addresses": {},
      "address": "EPXx1ZVKDtYshgwiwzJ2RrJohnmRyzg6GZPgc4NY2Ybe",
      "twitterId": "1520067044732940289",
      "discord": "vince_2.",
      "twitter": "BarackObama099",
      "discordId": "1188212330522230824",
      "connectedWallet": "0x399dac0A190C5CBE0913cA88Fd62Db907422239E"
    },
    {
      "userId": "b3337a1d-f832-4b7c-8204-0cca693c6d71",
      "xp": 11,
      "name": "SNKVJ",
      "avatar": "https://cdn.discordapp.com/avatars/980752115620261898/383a7ea39e793251e16f4bbff1fd39cf",
      "numberOfQuests": 3,
      "addresses": {},
      "address": "H3oCCUcsWm7S7y81fdmwBbtfVSNTPJvRjnpAtoYeuy37",
      "twitterId": "1050407288756830209",
      "discord": "snkvj1984",
      "twitter": "snkumaran84",
      "discordId": "980752115620261898",
      "connectedWallet": "0x9b0B5d012d79DeA4F094E1c86CED0D97b2c7479f"
    },
    {
      "userId": "b78287f0-f0d5-4c69-85ae-82ba295c02aa",
      "xp": 11,
      "name": "carbonless",
      "avatar": "https://cdn.discordapp.com/avatars/390047392520470539/25fa19a374f417395c8c58615e19900e",
      "numberOfQuests": 3,
      "addresses": {},
      "address": "CwYGXsPiw8e6Urr5FebTX3dFWGUqdi73u7QZ8NNB8w4U",
      "twitterId": "1459391774418292738",
      "discord": "carbonless",
      "twitter": "carbonlesss",
      "discordId": "390047392520470539",
      "connectedWallet": "0xB8D5A345C1a47167B1326D153aC9C6779041996B"
    },
    {
      "userId": "69ff0aed-528c-4f91-b1c7-54386df9912e",
      "xp": 11,
      "name": "0xF8…a728",
      "avatar": "https://zealy-webapp-images-prod.s3.eu-west-1.amazonaws.com/public/69ff0aed-528c-4f91-b1c7-54386df9912e-1680303151052.jpg",
      "numberOfQuests": 3,
      "addresses": {},
      "address": "4BcXTRBS5YtrVqhMaFZJXfJrtFTtiAEU8WpZyoTEoMEs",
      "twitterId": "1639279383473946624",
      "discord": "nightfall001x1",
      "twitter": "redairdrop97654",
      "discordId": "689800453168431134",
      "connectedWallet": "0xF8ac35171E95B36b617112D1EAe2ED3F8A7ba728"
    },
    {
      "userId": "4500ec82-d74b-4feb-93c0-27a86281597f",
      "xp": 11,
      "name": "Ernie123",
      "avatar": "https://zealy-webapp-images-prod.s3.eu-west-1.amazonaws.com/public/4500ec82-d74b-4feb-93c0-27a86281597f-logo.png",
      "numberOfQuests": 3,
      "addresses": {},
      "address": "Epr8FW7G5mtNTVASizSz3DfGGTYQZk4SSTYXeLBQ2SYH",
      "twitterId": "1519439584484298752",
      "discord": "choupapi143",
      "twitter": "EstongOfficial",
      "discordId": "1033310060505481286",
      "connectedWallet": "0x2a5F86926D3564e2d9554c54CA5F62eD71e00fAc"
    },
    {
      "userId": "11dce3ca-1977-403f-9f6d-b6a6309c4889",
      "xp": 6,
      "name": "phil2018",
      "avatar": "https://cdn.discordapp.com/avatars/831028012605636610/1774bef6aea038ce5496260a2e390fde",
      "numberOfQuests": 2,
      "addresses": {},
      "address": "8qzggzAHcHiW4JuG3Ekjf6HwyV5f2puZPRH7neEcFQw",
      "twitterId": "4872644772",
      "discord": "phil2018",
      "twitter": "thimoteusu",
      "discordId": "831028012605636610",
      "connectedWallet": "0xC4ebD13f194041963b6684FCfC925FA07B69df1B"
    },
    {
      "userId": "bd5d69fd-5ebe-4e41-97de-10514d0face3",
      "xp": 1,
      "name": "rvandeuli02 l RVAndrian02",
      "avatar": "https://zealy-webapp-images-prod.s3.eu-west-1.amazonaws.com/public/bd5d69fd-5ebe-4e41-97de-10514d0face3-logo.png",
      "numberOfQuests": 1,
      "addresses": {},
      "address": "7bigYWFBTWaE99Dw9pHGq9F3oMLtaF1A5gN8eUsGV6qM",
      "twitterId": "1651102426194411521",
      "discord": "rvandeuli02",
      "twitter": "BPAnd15",
      "discordId": "1088250216379072592",
      "connectedWallet": "0x63eB4787A675dc43bBD45627FaB36a3F7f2f0aFA"
    }
  ];

  try {

    leaderboard.value = response.map((item, index) => {
      return {
        avatar: item.avatar,
        rank: index + 1,
        name: item.name,
        xp: item.xp,
        quests: item.numberOfQuests
      }
    });

  } catch (e) {
    console.log(e);
  }

})
</script>



<template>
  <div class="overflow-hidden">
    <div class="absolute top-0 left-0 right-0 bottom-0 opacity-30 h-screen -z-10 overflow-hidden">
      <video id="bg_img" src="/background_hero_animation.mp4" autoplay loop class="min-h-screen object-cover opacity-10" />
    </div>
    <div class="basis-full flex flex-col">
      <div class="space-y-8">
        <h1 class="text-4xl font-bold text-orange-400 w-full">Leaderboard </h1>
        <p class="text-lg">
          The leaderboard displays all contributors within MSHIBA community ranked by XP. The experience will be calculated based on the completed quests and any extra XP provided through our proprietary Telegram bot (coming soon).
        </p>

        <UAccordion
            color="orange"
            :ui="{item: {padding: 'pl-3'}}"
            variant="link"
            multiple
            :items="accordionItems">
          <template #default="{ item, index, open }">
            <UButton variant="link" class="border-b border-orange-400/50 text-white hover:bg-orange-900/10 hover:no-underline" :ui="{ rounded: 'rounded-none', padding: { sm: 'p-3' } }">
              <span class="truncate text-orange-100 uppercase">{{ index + 1 }}. {{ item.label }}</span>

              <template #trailing>
                <UIcon
                    name="i-heroicons-chevron-right-20-solid"
                    class="w-5 h-5 ms-auto transform transition-transform duration-200 text-white"
                    :class="[open && 'rotate-90']"
                />
              </template>
            </UButton>
          </template>

          <template #item="{ item }">
            <p class="italic text-orange-100">
              {{ item.content }}
            </p>
          </template>
        </UAccordion>
      </div>

      <div class="mt-8">
        <UTable class="w-full" :columns="leaderboardColumns" :rows="rows">

          <template #profile-data="{row}">
            <div class="flex space-x-2 items-center">
              <img :src="row.avatar" class="h-8 w-8 rounded-full" />
              <span>{{row.name}}</span>
            </div>
          </template>

          <template #name-data="{row}">
            {{ row.name }}
          </template>

          <template #rank-data="{row}">
            {{ row.rank }}
          </template>
        </UTable>

        <div class="flex justify-end px-3 py-3.5 border-t border-gray-200 dark:border-gray-700">
          <UPagination v-model="page" :page-count="pageCount" :total="leaderboard.length" />
        </div>
      </div>
    </div>
  </div>

</template>