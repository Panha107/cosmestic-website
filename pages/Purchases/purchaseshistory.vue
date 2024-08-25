<template>
  <div class="w-full h-[700px] my-5 flex flex-col items-center gap-4">
    <h3 class="text-4xl font-sans font-bold">Product history</h3>
    <div class="w-[30%] text-base text-gray-400 flex items-center p-3">
      Check the status of recent orders, manage returns, and discover similar
      products.
    </div>
    <div class="flex flex-col gap-4 w-[55%] p-4 px-6 rounded-[10px] border">
      <div class="flex justify-between">
        <div class="flex gap-2 *:text-base">
          <span class="text-gray-300">Delivery on March 22,2021</span>
          <span class="font-bold">Order #4376</span>
        </div>
        <div
          class="w-[45%] flex items-center justify-between *:text-sm *:text-gray-500"
        >
          <NuxtLink to="" class="underline">Manage order</NuxtLink>
          <NuxtLink to="" class="underline">View invoice</NuxtLink>
          <svg
            data-accordion-icon
            class="w-[15px] rotate-180 shrink-0"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 10 6"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 5 5 1 1 5"
            />
          </svg>
        </div>
      </div>
      <div class="flex justify-between items-center">
        <div class="flex items-center gap-4">
          <img class="w-28" src="/assets/images/product1.png" alt="" />
          <div class="flex flex-col gap-1">
            <span class="text-base font-bold">Product name</span>
            <div class="flex gap-2">
              <span
                class="text-xs text-gray-500 bg-slate-200 p-1 px-2 rounded-xl"
                >x2 items</span
              >
              <span
                class="text-xs text-gray-500 bg-slate-200 p-1 px-2 rounded-xl"
                >50ml</span
              >
            </div>
            <span class="text-base font-semibold">$104</span>
          </div>
        </div>
        <div class="flex flex-col gap-2">
          <NuxtLink class="text-xs bg-green-800 px-5 text-white py-2 rounded"
            >Buy again</NuxtLink
          >
          <NuxtLink class="text-xs bg-gray-100 px-5 py-2 rounded"
            >View product</NuxtLink
          >
        </div>
      </div>
      <div class="flex justify-between items-center">
        <div class="flex items-center gap-4">
          <img class="w-28" src="/assets/images/product2.png" alt="" />
          <div class="flex flex-col gap-1">
            <span class="text-base font-bold">Product name</span>
            <div class="flex gap-2">
              <span
                class="text-xs text-gray-500 bg-slate-200 p-1 px-2 rounded-xl"
                >x2 items</span
              >
              <span
                class="text-xs text-gray-500 bg-slate-200 p-1 px-2 rounded-xl"
                >50ml</span
              >
            </div>
            <span class="text-base font-semibold">$76</span>
          </div>
        </div>
        <div class="flex flex-col gap-2">
          <NuxtLink class="text-xs bg-green-800 px-5 text-white py-2 rounded"
            >Buy again</NuxtLink
          >
          <NuxtLink class="text-xs bg-gray-100 px-5 py-2 rounded"
            >View product</NuxtLink
          >
        </div>
      </div>
    </div>

    <div class="flex flex-col gap-4 w-[55%] p-4 px-6 rounded-[10px] border">
      <div class="flex justify-between">
        <div class="flex gap-2 *:text-base">
          <span class="font-bold">Order #4376</span>
          <span class="text-gray-300">Delivery on March 22,2021</span>
        </div>
        <div
          class="w-[45%] flex items-center justify-between *:text-sm *:text-gray-500"
        >
          <NuxtLink to="" class="underline">Manage order</NuxtLink>
          <NuxtLink to="" class="underline">View invoice</NuxtLink>
          <svg
            data-accordion-icon
            class="w-[15px] rotate-90 shrink-0"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 10 6"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 5 5 1 1 5"
            />
          </svg>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-4 w-[55%] p-4 px-6 rounded-[10px] border">
      <div class="flex justify-between">
        <div class="flex gap-2 *:text-base">
          <span class="font-bold">Order #4376</span>
          <span class="text-gray-300">Delivery on March 22,2021</span>
        </div>
        <div
          class="w-[45%] flex items-center justify-between *:text-sm *:text-gray-500"
        >
          <NuxtLink to="" class="underline">Manage order</NuxtLink>
          <NuxtLink to="" class="underline">View invoice</NuxtLink>
          <svg
            data-accordion-icon
            class="w-[15px] rotate-90 shrink-0"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 10 6"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 5 5 1 1 5"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>
