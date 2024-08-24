<template>
  <div class="w-full h-[422px]">
    <div class="w-[1300px] h-full mx-auto px-16 grid grid-cols-3 gap-4 py-3">
      <div class="p-1 flex flex-col justify-center gap-6">
        <h2 class="text-2xl font-bold">Read What’s New</h2>
        <p class="text-lg">
          Sint consequat in ipsum irure adipisicing dolore culpa incididunt.
          Veniam elit magna anim ipsum eiusmod eu
        </p>
        <div class="flex justify-between">
          <button
            class="text-[#459D7A] w-fit p-[7px_37px_7px_37px] border border-emerald-600 rounded"
          >
            Explore more
          </button>
          <button class="flex items-center gap-5">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="25px"
              viewBox="0 -960 960 960"
              width="25px"
              fill="#059669"
            >
              <path
                d="m294.92-450 227.85 227.85L480-180 180-480l300-300 42.77 42.15L294.92-510H780v60H294.92Z"
              />
            </svg>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="24px"
              viewBox="0 -960 960 960"
              width="24px"
              fill="#4B77D1"
            >
              <path
                d="M665.08-450H180v-60h485.08L437.23-737.85 480-780l300 300-300 300-42.77-42.15L665.08-450Z"
              />
            </svg>
          </button>
        </div>
      </div>
      <div
        class="flex flex-col rounded-lg overflow-hidden shadow-[3px_4px_4px_0px_#00000040]"
      >
        <img class="h-[15rem]" src="/assets/images/detail.png" alt="" />
        <p class="p-5 text-base">Anim sint Lorem excepteur commodo</p>
        <span class="pl-5 pt-8 text-gray-500">Oct 12, 2022</span>
      </div>
      <div
        class="flex flex-col rounded-lg overflow-hidden shadow-[3px_4px_4px_0px_#00000040]"
      >
        <img class="h-[15rem]" src="/assets/images/detail2.png" alt="" />
        <p class="p-5 text-base">Anim sint Lorem excepteur commodo</p>
        <span class="pl-5 pt-8 text-gray-500">Oct 12, 2022</span>
      </div>
    </div>
  </div>
</template>
