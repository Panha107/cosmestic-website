<template>
  <div class="w-full bg-[#1D2128]">
    <footer
      class="grid grid-cols-2 w-[1300px] mx-auto p-16 h-[400px] text-white racking-widest"
    >
      <div class="grid grid-cols-3">
        <div class="flex flex-col gap-3">
          <NuxtLink class="font-semibold" to="/">About</NuxtLink>
          <NuxtLink to="/">Home</NuxtLink>
          <NuxtLink to="/">Shop</NuxtLink>
          <NuxtLink to="/">Our story</NuxtLink>
          <NuxtLink to="/">Blog</NuxtLink>
          <select
            class="border border-solid border-[#DEE1E6] rounded-md p-1 w-24   bg-[#1D2128]"
            name="languages"
            id="languages"
          >
            <option value="english">English</option>
          </select>
        </div>
        <div class="flex flex-col gap-3">
          <NuxtLink class="font-semibold" to="/">Help</NuxtLink>
          <NuxtLink to="/">Shipping & Return</NuxtLink>
          <NuxtLink to="/">Track Order</NuxtLink>
          <NuxtLink to="/">FAQs</NuxtLink>
        </div>
        <div class="flex flex-col gap-3">
          <p class="font-semibold">Contact</p>
          <span>Phone:</span>
          <span>(+1) 123 456 7893</span>
          <span>Email:</span>
          <span>name@gmail.com</span>
        </div>
      </div>
      <div class="flex flex-col gap-4 pl-[7rem]">
        <p>Receive new promotions</p>
        <p>Duis ea tempor commodo amet reprehende</p>
        <div class="relative flex items-center">
          <img class="absolute pl-2" src="/assets/icons/mail.svg" alt="" />
          <input
            class="pl-[2.6rem] p-[12px_115px_11px_20px] rounded-l-lg rounded-r-none border border-solid border-[#9095A0] bg-[#1D2128] placeholder-gray-400"
            type="email"
            placeholder="Input your email"
          />
          <button
            class="p-[12.06px_19px_11.94px_20px] rounded-r-lg rounded-l-none bg-[#459D7A]"
          >
            Subscribe
          </button>
        </div>
        <div class="flex gap-4 mt-3">
          <NuxtLink
            ><img src="/assets/images/inlink.png" class="w-6 h-5" alt=""
          /></NuxtLink>
          <NuxtLink
            ><img src="/assets/images/fb.png" class="w-6 h-5" alt=""
          /></NuxtLink>
          <NuxtLink
            ><img src="/assets/images/twitter.png" class="w-6 h-5" alt=""
          /></NuxtLink>
          <NuxtLink to="https://www.youtube.com/"
            ><img src="/assets/images/youtube.png" class="w-6 h-5" alt=""
          /></NuxtLink>
        </div>
        <div class="flex gap-3 mt-3">
          <p>© 2022 Brand, Inc.</p>
          <p>• Privacy</p>
          <p>• Terms</p>
          <p>• Sitemap</p>
        </div>
      </div>
    </footer>
  </div>
</template>
