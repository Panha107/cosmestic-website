<script setup>
import { products } from "~/content/allData.js";
const displayedProducts = products.slice(0, 16);
</script>
<template>
  <div class="w-full h-[1796px] m-8">
    <div class="pt-4 flex flex-col gap-5">
      <div class="flex justify-between w-[1300px] mx-auto px-14 pt-5">
        <div class="flex items-center">
          <button
            class="p-[12px_39.5px_12px_38.5px] rounded cursor-pointer text-[#459D7A] hover:text-white hover:bg-[#459D7A] ease-in-out duration-300"
          >
            All Product</button
          ><span class="text-gray-400 text-2xl">|</span>
          <button
            class="p-[12px_39.5px_12px_38.5px] rounded cursor-pointer text-[#459D7A] hover:text-white hover:bg-[#459D7A] ease-in-out duration-300"
          >
            Face
          </button>
          <span class="text-gray-400 text-2xl">|</span>
          <button
            class="p-[12px_39.5px_12px_38.5px] rounded cursor-pointer text-[#459D7A] hover:text-white hover:bg-[#459D7A] ease-in-out duration-300"
          >
            Body
          </button>
        </div>
        <div class="relative flex items-center gap-6">
          <svg
            class="absolute left-4"
            xmlns="http://www.w3.org/2000/svg"
            height="24px"
            viewBox="0 -960 960 960"
            width="24px"
            fill="#2c6368"
          >
            <path
              d="M784-120 532-372q-30 24-69 38t-83 14q-109 0-184.5-75.5T120-580q0-109 75.5-184.5T380-840q109 0 184.5 75.5T640-580q0 44-14 83t-38 69l252 252-56 56ZM380-400q75 0 127.5-52.5T560-580q0-75-52.5-127.5T380-760q-75 0-127.5 52.5T200-580q0 75 52.5 127.5T380-400Z"
            />
          </svg>
          <input
            class="pl-[3.2rem] text-lg px-2 py-[0.65rem] border rounded-md placeholder-gray-300"
            type="text"
            placeholder="search product..."
          />
          <button
            class="flex items-center gap-3 border px-4 py-[10px] bg-[#F3F4F6] text-lg text-[#565E6C] rounded-md font-mono"
          >
            Sort
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="24px"
              viewBox="0 -960 960 960"
              width="24px"
              fill="#565E6C"
            >
              <path
                d="M400-240v-80h160v80H400ZM240-440v-80h480v80H240ZM120-640v-80h720v80H120Z"
              />
            </svg>
          </button>
        </div>
      </div>
      <div class="w-[1300px] mx-auto px-14 pt-5">
        <div class="grid grid-cols-4 gap-6">
          <div
            class="shadow-[3px_4px_4px_0px_#00000040] rounded-lg"
            v-for="(product, index) in displayedProducts"
            :key="index"
          >
            <div class="relative">
              <span
                v-if="product.tag"
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
                  <p
                    v-if="product.discountPrice"
                    class="text-[#6E7787] text-sm line-through"
                  >
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
