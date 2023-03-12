<script setup>
import {ref} from "vue";

const wallets = ref([
  {
    icon: 'ETH',
    network: 'Ethernet',
    chart: 'chart.svg',
    price: '1,590.02 USDT',
    subPrice: '+4.23%',
    balance: '120 ETH',
    calculatedBalance: '≈185,238.28 USDT',
  },
  {
    icon: 'BNB',
    network: 'BSC',
    chart: 'chart.svg',
    price: '309.50 USDT',
    subPrice: '+2.52%',
    balance: '1,092.12 BNB',
    calculatedBalance: '≈34,496.18 USDT',
  },
  {
    icon: 'USDT',
    network: 'Tether US',
    chart: 'chart.svg',
    price: '1 USDT',
    subPrice: '-2.01%',
    balance: '3,566.16 USDT',
    calculatedBalance: '≈3,566.16 USDT',
  },{
    icon: 'Bitcoin',
    network: 'Bitcoin',
    chart: 'chart.svg',
    price: '23,277.97 USDT',
    subPrice: '+7.22%',
    balance: '0.014 BTC',
    calculatedBalance: '≈352 USDT',
  },{
    icon: 'USDC',
    network: 'USD Coin',
    chart: 'chart.svg',
    price: '1 USDT',
    subPrice: '-5.02%',
    balance: '142 USDC',
    calculatedBalance: '≈100.00 USDT',
  },{
    icon: 'DOGE',
    network: 'Dogecoin',
    chart: 'chart.svg',
    price: '0.087827 USDT',
    subPrice: '-2.55%',
    balance: '0 DOGE',
    calculatedBalance: '≈185,238.28 USDT',
  },{
    icon: 'TRX',
    network: 'Tron',
    chart: 'chart.svg',
    price: '0.06357000 USDT',
    subPrice: '+5.22%',
    balance: '0 TRX',
    calculatedBalance: '≈185,238.28 USDT',
  },
])

</script>

<template>
  <div class="max-w-[688px] min-w-[375px] h-[674px] dark:bg-[#0C1C33] rounded-[20px] ml-[30px] mt-[30px] bg-[#FFFFFF] max-[375px]:h-[690px] dark:max-[375px]:bg-[#071222] ">
    <div class="container max-w-[668px] h[662px]  pl-[28px] pt-[20px] relative ">
      <div class="flex justify-between  max-w-[640px] pl-[4px]">
        <div>
          <span class="text-[16px] leading-6 font-semibold text-[#039AB6]">Wallet</span>
          <div class="flex items-end">
            <span class="font-bold text-[24px] leading-[30px] dark:text-[#E6E7E9] text-[#101415] font-robotoMono">223,652.62</span>
            <div class="flex items-center pl-[10px]">
              <span class="dark:text-[#E6E7E9] text-[#101415]">USDT</span>
              <img src="src/assets/icons/arrow-down.svg">
            </div>
          </div>
        </div>
        <div class="h-[24px] ">
          <img src="src/assets/icons/info.svg">
        </div>
      </div>
      <div class="flex justify-between pt-[16px] ">
        <div class="flex">

          <div class="pr-[10px]">
            <button class="flex  flex-row items-center justify-center w-[124px] h-[40px] max-[375px]:w-[112px]  gap-[8px] border-[1px] rounded-[99px] border-[#004E68]">
              <img src="src/assets/icons/deposit.svg">
              <span class="font-medium text-[14px] leading-6 text-[#039AB6]">Deposit</span>
            </button >
          </div>
          <div>
            <button class="flex  flex-row items-center justify-center w-[137px] h-[40px] max-[375px]:w-[125px]  gap-[8px] border-[1px] rounded-[99px] border-[#004E68]">
              <img src="src/assets/icons/withdraw.svg">
              <span class="font-medium text-[14px] leading-6 text-[#039AB6]">Withdraw</span>
            </button>
          </div>

        </div>
        <div class=" ">
          <button class="flex pt-[8px]  ">
            <span class="pr-[8px] font-medium text-[14px] leading-6 text-[#039AB6]">To wallet</span>
            <img class="max-[375px]:hidden" src="src/assets/icons/arrow-right.svg">
          </button>



        </div>
      </div>
      <table class=" w-full   overflow-x-auto ">
        <thead class="sticky top-0 left-0 ">
        <tr class=" ">
          <th class=" sticky top-0 left-0 ">
            <span class="text-[12px] leading-[14px] font-medium text-[#6E8BB5]">Asset</span>
          </th>
          <th class="  ">
            <span class="text-[12px] leading-[14px] font-medium font-interMedium text-[#6E8BB5]">Trend 24h</span>
          </th>
          <th class=" ">
            <div class="flex items-center justify-center">
            <span class="text-[12px] leading-[14px] text-[#6E8BB5]">Price</span>
            <img src="src/assets/icons/sort.svg">
            </div>

          </th>
          <th class="  ">
            <div class="flex items-center justify-center">
            <span class="text-[12px] leading-[14px] text-[#6E8BB5]">Balance</span>
            <img src="src/assets/icons/sort.svg">
            </div>
          </th>
        </tr>
        </thead>
        <tbody>
        <tr v-for="({icon, network, price, subPrice, balance, calculatedBalance}, index ) in wallets" :key="index" class="flex flex-row  justify-between max-w-[640px] h-[64px] pl-[4px] pt-[10px] border-b-[1px] dark:border-b-[#172E4F] border-b-[#CDEBF0] ">
          <td class=" sticky top-0 left-0 ">
            <div class="flex items-center w-[120px] h-[44px] pl-[8px] ">
              <figure>
                <img :src="`/img/icons/${icon}.png`" alt="">
              </figure>
              <div class="flex flex-col pl-[12px] ">
                <span class="dark:text-[#E6E7E9] text-[#101415] text-[15px] leading-6 font-semibold">{{icon}}</span>
                <span class="leading-5 text-[13px] font-medium dark:text-[#6E8BB5] text-[#565A5B]">{{network}}</span>
              </div>
            </div>
          </td>
          <td class="">
            <figure class="w-[110px]">
            <img class="" src="../assets/icons/chart.svg" alt="">
            </figure>
          </td>
          <td >
            <div class="flex flex-col w-[140px] h-[44px] ">
              <span class="dark:text-[#E6E7E9] text-[#101415] text-[15px] leading-6 font-semibold">{{price}}</span>
              <span class="leading-5 text-[13px] font-medium " :class="[subPrice.includes('-')?'text-[#C50000]':'text-[#138D00]']">{{subPrice}}</span>
            </div>
          </td>
          <td class="">
            <div class="flex flex-col w-[145px] h-[44px] ">
              <span class="dark:text-[#E6E7E9] text-[#101415] text-[15px] leading-6 font-semibold">{{balance}}</span>
              <span class="leading-5 text-[13px] font-medium dark:text-[#6E8BB5] text-[#565A5B]">{{calculatedBalance}}</span>
            </div>
          </td>
        </tr>

        </tbody>
      </table>
      <div class="flex  justify-end max-w-[668px] ">
        <div class="flex pt-[8px]">
          <button class="flex  items-center justify-center hover:text-[#039AB6] hover:bg-[#112440] hover:rounded-[8px] w-[28px] h-[32px] text-[13px] leading-5 font-medium text-[#5B7398]">1</button>
          <button class="flex  items-center justify-center hover:text-[#039AB6] hover:bg-[#112440] hover:rounded-[8px] w-[28px] h-[32px] text-[13px] leading-5 font-medium text-[#5B7398]">2</button>
          <button class="flex  items-center justify-center hover:text-[#039AB6] hover:bg-[#112440] hover:rounded-[8px] w-[28px] h-[32px] text-[13px] leading-5 font-medium text-[#5B7398]">3</button>
        </div>
      </div>
    </div>


  </div>
</template>
