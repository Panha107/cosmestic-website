<template>
  <div class="w-full h-[710px] mb-4">
    <div class="w-[88%] mx-auto">
      <ul class="flex items-center gap-2 text-base text-[#000000CC] mt-[89px]">
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="20px"
          viewBox="0 -960 960 960"
          width="20px"
          fill="#5f6368"
        >
          <path d="M522-480 333-669l51-51 240 240-240 240-51-51 189-189Z" />
        </svg>
        <li>
          <NuxtLink>Shop</NuxtLink>
        </li>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="20px"
          viewBox="0 -960 960 960"
          width="20px"
          fill="#5f6368"
        >
          <path d="M522-480 333-669l51-51 240 240-240 240-51-51 189-189Z" />
        </svg>
        <li>
          <NuxtLink>Product Type</NuxtLink>
        </li>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="20px"
          viewBox="0 -960 960 960"
          width="20px"
          fill="#5f6368"
        >
          <path d="M522-480 333-669l51-51 240 240-240 240-51-51 189-189Z" />
        </svg>
        <li>
          <NuxtLink>Detail</NuxtLink>
        </li>
      </ul>
      <div class="grid grid-cols-2 mt-4">
        <div class="flex gap-1">
          <div class="flex gap-[12px] flex-col">
            <img
              v-for="(images, index) in pictures"
              :key="index"
              :src="images"
              alt="images"
              class="w-[100px] h-[125px] overflow-hidden rounded"
            />
          </div>
          <span
            class="absolute bg-yellow-400 text-yellow-700 text-sm p-[6px_9px_6px_9px] rounded-xl left-[540px]"
            >{{ product.tag }}</span
          >
          <img
            :src="product.img"
            :alt="product.title"
            class="w-[437px] h-[536px] object-cover rounded"
          />
        </div>
        <div class="flex flex-col gap-[15px]">
          <h2 class="text-2xl font-medium">Product Name</h2>
          <p>Aliquip fugiat ipsum nostrud ex et eu incididunt</p>
          <div class="flex items-center gap-4 mt-3">
            <p class="text-4xl font-bold text-[#459D7A]">
              {{ product.price }}
            </p>
            <p class="text-xl text-[#9095A0]">{{ product.discountPrice }}</p>
          </div>
          <p class="text-base">
            In ullamco labore mollit et exercitation fugiat exercitation minim
            ex sint ullamco exercitation amet officia mollit. Qui cillum
            pariatur in con
          </p>
          <div class="flex gap-4">
            <p class="font-bold">
              368 <span class="text-[#9095A0] font-normal">reviews</span>
            </p>
            <p class="font-bold">
              823 <span class="text-[#9095A0] font-normal">sold</span>
            </p>
          </div>
          <div class="flex gap-2">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="24px"
              viewBox="0 -960 960 960"
              width="23px"
              fill="#48752C"
            >
              <path
                d="m429-336 238-237-51-51-187 186-85-84-51 51 136 135Zm51 240q-79 0-149-30t-122.5-82.5Q156-261 126-331T96-480q0-80 30-149.5t82.5-122Q261-804 331-834t149-30q80 0 149.5 30t122 82.5Q804-699 834-629.5T864-480q0 79-30 149t-82.5 122.5Q699-156 629.5-126T480-96Zm0-72q130 0 221-91t91-221q0-130-91-221t-221-91q-130 0-221 91t-91 221q0 130 91 221t221 91Zm0-312Z"
              />
            </svg>
            <p>Free shipping on orders over $49USD</p>
          </div>
          <div class="flex gap-2">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="24px"
              viewBox="0 -960 960 960"
              width="23px"
              fill="#48752C"
            >
              <path
                d="m429-336 238-237-51-51-187 186-85-84-51 51 136 135Zm51 240q-79 0-149-30t-122.5-82.5Q156-261 126-331T96-480q0-80 30-149.5t82.5-122Q261-804 331-834t149-30q80 0 149.5 30t122 82.5Q804-699 834-629.5T864-480q0 79-30 149t-82.5 122.5Q699-156 629.5-126T480-96Zm0-72q130 0 221-91t91-221q0-130-91-221t-221-91q-130 0-221 91t-91 221q0 130 91 221t221 91Zm0-312Z"
              />
            </svg>
            <p>Free + easy returns</p>
          </div>
          <div class="flex flex-col gap-1">
            <p class="text-base font-medium">Choose size</p>
            <select
              id="small"
              class="block w-full py-2 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            >
              <option value="50ml">50.00 ML</option>
            </select>
          </div>
          <div class="flex flex-col gap-1">
            <label class="text-base font-medium">Quantity</label>
            <div class="flex gap-2 items-center">
              <button class="border px-3 rounded text-lg bg-[#F3F4F6]">
                -
              </button>
              <span class="border px-3 rounded text-lg bg-[#F3F4F6]">1</span>
              <button class="border px-3 rounded text-lg bg-[#F3F4F6]">
                +
              </button>
            </div>
          </div>
          <div class="w-full flex gap-5">
            <button
              class="flex items-center justify-center gap-4 w-[50%] py-2.5 rounded-lg text-lg text-[#459D7A] border border-[#459D7A]"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#459D7A"
              >
                <path
                  d="M444-576v-132H312v-72h132v-132h72v132h132v72H516v132h-72ZM263.79-96Q234-96 213-117.21t-21-51Q192-198 213.21-219t51-21Q294-240 315-218.79t21 51Q336-138 314.79-117t-51 21Zm432 0Q666-96 645-117.21t-21-51Q624-198 645.21-219t51-21Q726-240 747-218.79t21 51Q768-138 746.79-117t-51 21ZM48-792v-72h133l155 360h301l113-264h78L703-476q-9 20-26.5 32T637-432H317l-42 72h493v72H276q-42 0-63-36.5t0-71.5l52-90-131-306H48Z"
                />
              </svg>
              Add to bag
            </button>
            <button
              class="w-[50%] py-2.5 rounded-lg text-lg text-white bg-[#459D7A]"
            >
              Checkout
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { products } from "~/content/allData";
const product = products[0];
import img1 from "~/assets/images/pro2.png";
import img2 from "~/assets/images/detail.png";
import img3 from "~/assets/images/pro3.png";
import img4 from "~/assets/images/image35.png";
const pictures = [img1, img2, img3, img4];
</script>
