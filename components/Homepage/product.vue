<script setup>
import { products } from "~/content/data.js";
</script>
<template>
  <div class="w-full h-[665px]">
    <div class="pt-4 flex flex-col gap-5">
      <h1 class="flex justify-center text-[30px] font-semibold">
        Our Products
      </h1>
      <div class="flex justify-center">
        <button
          class="p-[7px_25.25px_7px_36.25px] rounded text-white bg-[#459D7A]"
        >
          Best-sellers
        </button>
        <button class="p-[7px_15.75px_7px_28.75px] rounded text-[#459D7A]">
          New product
        </button>
      </div>
      <div class="w-[1300px] mx-auto px-14 pt-5">
        <div class="grid grid-cols-4 gap-6">
          <div
            class="shadow-[3px_4px_4px_0px_#00000040] rounded-lg"
            v-for="(product, index) in products"
            :key="index"
          >
            <div class="relative">
              <span
                class="absolute p-[6px_9px_6px_9px] rounded-lg bg-[#FFC970] text-[#774900] overflow-hidden top-3 right-3"
                >{{ product.tag }}</span
              >
              <img
                class="w-full h-80 object-cover rounded-t-lg"
                :src="product.img"
                :alt="product.title"
              />
            </div>
            <div class="p-3 flex flex-col gap-3">
              <p class="font-semibold">{{ product.title }}</p>
              <p class="text-gray-600">{{ product.description }}</p>
              <div class="flex items-center justify-between">
                <div class="flex gap-2 items-center">
                  <p class="text-lg font-semibold text-gray-800">
                    {{ product.price }}
                  </p>
                  <p class="text-[#6E7787] text-sm line-through">
                    {{ product.discountPrice }}
                  </p>
                </div>
                <button
                  class="border p-2 rounded-full border-[#459D7A]"
                  type="submit"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    height="20px"
                    viewBox="0 -960 960 960"
                    width="20px"
                    fill="#459D7A"
                  >
                    <path
                      d="M292.31-115.38q-25.31 0-42.66-17.35-17.34-17.35-17.34-42.65 0-25.31 17.34-42.66 17.35-17.34 42.66-17.34 25.31 0 42.65 17.34 17.35 17.35 17.35 42.66 0 25.3-17.35 42.65-17.34 17.35-42.65 17.35Zm375.38 0q-25.31 0-42.65-17.35-17.35-17.35-17.35-42.65 0-25.31 17.35-42.66 17.34-17.34 42.65-17.34t42.66 17.34q17.34 17.35 17.34 42.66 0 25.3-17.34 42.65-17.35 17.35-42.66 17.35ZM235.23-740 342-515.38h265.38q6.93 0 12.31-3.47 5.39-3.46 9.23-9.61l104.62-190q4.61-8.46.77-15-3.85-6.54-13.08-6.54h-486Zm-19.54-40h520.77q26.08 0 39.23 21.27 13.16 21.27 1.39 43.81l-114.31 208.3q-8.69 14.62-22.58 22.93-13.88 8.31-30.5 8.31H324l-48.62 89.23q-6.15 9.23-.38 20 5.77 10.77 17.31 10.77h435.38v40H292.31q-35 0-52.23-29.5-17.23-29.5-.85-59.27l60.15-107.23L152.31-820H80v-40h97.69l38 80ZM342-515.38h280-280Z"
                    />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
