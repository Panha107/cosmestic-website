<template>
  <div>
    <div class="w-[1300px] mx-auto">
      <nav class="flex items-center w-full h-[60px] justify-between px-9">
        <h2 class="text-[20px] font-semibold">Company-Name</h2>

        <div class="h-full flex justify-center items-center px-8">
          <ul class="flex gap-[15px]">
            <li>
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/shop">Shop</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/offers">Offers</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/ourstory">Our Story</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/blog">Blog</NuxtLink>
            </li>
          </ul>
          <div class="relative flex items-center pl-7 gap-3">
            <img
              class="absolute pl-2"
              src="/assets/icons/search.svg"
              alt="search"
            />
            <input
              class="pl-[2.6rem] p-[1.5px] border rounded-md"
              type="text"
              placeholder="Search product.."
            />
            <div class="flex gap-2.5">
              <NuxtLink to="/order">
                <img
                  class="border"
                  src="/assets/icons/shopping_cart.svg"
                  alt=""
                />
              </NuxtLink>
              <span class="font-semibold">Cart (0)</span>
            </div>
            <img class="border" src="/assets/icons/user.svg" alt="" />
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>
<script setup>
import shop from "~/pages/shop.vue";
</script>
<style scoped>
.router-link-exact-active {
  color: rgb(0, 218, 0);
}
</style>
