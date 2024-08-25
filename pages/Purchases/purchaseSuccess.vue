<template>
  <div class="w-full h-[95%] my-5 flex flex-col items-center gap-4">
    <h3 class="text-4xl font-sans font-bold">Thank you for your purchase!</h3>
    <span class="text-base text-gray-400"
      >You will receive an confirmation letter through your email</span
    >
    <div class="flex flex-col gap-4 w-[55%] p-4 px-8 rounded-[10px] border">
      <div
        class="flex flex-col gap-4 *:flex *:justify-between text-base text-gray-400"
      >
        <div class="">Data <span class="text-black">27/04/2022</span></div>
        <div class="">
          Customer <span class="text-black">Alvaro Garcia</span>
        </div>
        <div class="">
          Payment Method
          <img class="w-8" src="/assets/images/masterCard.svg" alt="" />
        </div>
        <div class="border text-xs"></div>
        <div class="">
          Order Number <span class="text-black">732-123-4567</span>
        </div>
        <div class="">
          Total <span class="text-black text-2xl font-medium">$187</span>
        </div>
      </div>
      <span class="text-2xl font-bold text-black">Order Line</span>
      <div class="border"></div>
      <div class="flex items-center justify-between">
        <div
          class="flex items-center gap-5 *:text-xs *:text-gray-400 *:capitalize"
        >
          <img class="w-24" src="/assets/images/product1.png" alt="" />
          <div class="flex flex-col gap-[3px]">
            <span class="text-base font-bold text-black">Product name</span>
            <span>size: 50ml</span>
            <span>x2 items</span>
          </div>
        </div>
        <span class="text-base font-bold">$104</span>
      </div>
      <div class="flex items-center justify-between">
        <div
          class="flex items-center gap-5 *:text-xs *:text-gray-400 *:capitalize"
        >
          <img class="w-24" src="/assets/images/product2.png" alt="" />
          <div class="flex flex-col gap-[3px]">
            <span class="text-base font-bold text-black">Product name</span>
            <span>size: 50ml</span>
            <span>x1 items</span>
          </div>
        </div>
        <span class="text-base font-bold">$76</span>
      </div>
      <div class="flex items-center justify-between">
        <NuxtLink
          to="/order"
          class="border py-3 px-5 rounded-md text-lg text-white bg-green-900"
          >Continue shopping</NuxtLink
        >
        <NuxtLink
          to="/purchases/purchaseshistory"
          class="py-3 px-5 rounded-md text-lg bg-gray-200"
          >Purchases history</NuxtLink
        >
      </div>
    </div>
  </div>
</template>
