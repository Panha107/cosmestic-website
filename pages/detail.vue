<template>
  <div>
    <div class="w-full h-[800px]" id="benefits">
      <div class="w-[86%] mx-auto">
        <ul class="flex justify-center">
          <li class="px-16 py-2 text-lg rounded-md bg-[#C5E6D9] text-[#459D7A]">
            <NuxtLink to="#benefits">Benefits</NuxtLink>
          </li>
          <li
            class="px-14 py-2 text-lg text-[#459D7A] rounded-md cursor-pointer hover:bg-[#C5E6D9] ease-linear duration-300"
          >
            <NuxtLink to="#ingredients">Ingredients</NuxtLink>
          </li>
          <li
            class="px-14 py-2 text-lg text-[#459D7A] rounded-md cursor-pointer hover:bg-[#C5E6D9] ease-linear duration-300"
          >
            <NuxtLink to="#how-to-use">How to use</NuxtLink>
          </li>
          <li
            class="px-14 py-2 text-lg text-[#459D7A] rounded-md cursor-pointer hover:bg-[#C5E6D9] ease-linear duration-300"
          >
            <NuxtLink to="#reviews">Reviews</NuxtLink>
          </li>
          <li
            class="px-14 py-2 text-lg text-[#459D7A] rounded-md cursor-pointer hover:bg-[#C5E6D9] ease-linear duration-300"
          >
            <NuxtLink to="#faqs">FAQs</NuxtLink>
          </li>
        </ul>
        <div class="grid grid-cols-2 gap-16 mt-6">
          <div class="flex flex-col gap-6 justify-center">
            <h3 @click="scrollToTop" class="text-4xl font-medium">Benefits</h3>
            <p class="text-lg text-gray-500">
              Consectetur excepteur elit ullamco incididunt voluptate tempor
              exercitation. Lorem commodo ullamco quis velit officia aute
              laboris elit sit exercitation ut esse pariatur occaecat quis
            </p>

            <div class="flex flex-col gap-2">
              <h4 class="text-xl font-medium">Laboris consequat ad</h4>
              <p class="text-lg text-gray-500">
                Consectetur excepteur elit ullamco incididunt voluptate tempor
                exercitation. Lorem commodo ullamco quis velit officia aute
                laboris elit sit exercitation ut esse pariatur
              </p>
            </div>
            <div class="flex flex-col gap-2">
              <h4 class="text-xl font-medium">Duis duis do labore pariatur</h4>
              <p class="text-lg text-gray-500">
                Ad qui aliqua nulla nostrud consectetur laboris nostrud commodo
                voluptate. Lorem id qui laborum aute voluptate
              </p>
            </div>
            <div class="flex flex-col gap-2">
              <h4 class="text-xl font-medium">Deserunt ex</h4>
              <p class="text-lg text-gray-500">
                Cupidatat culpa id do laboris nisi aliqua eu. Veniam aliqua duis
                Lorem adipisicing et minim velit quis
              </p>
            </div>
          </div>
          <div
            class="w-[557px] h-[696px] object-cover overflow-hidden rounded-lg"
          >
            <img class="w-full h-full" src="/assets/images/pic.png" alt="" />
          </div>
        </div>
      </div>
    </div>

    <!-- ingredients -->
    <div class="w-full h-[562px]" id="ingredients">
      <div class="w-[86%] mx-auto">
        <h3 @click="scrollToTop" class="text-4xl font-medium">Ingredients</h3>
        <div class="my-5 mt-9 grid grid-cols-3">
          <div
            v-for="(item, index) in allpic"
            :key="index"
            class="w-[360px] h-[350px] border rounded-lg overflow-hidden shadow-[3px_4px_4px_0px_#00000040]"
          >
            <img
              class="w-full object-cover"
              :src="item.img"
              :alt="item.title"
            />
            <div class="flex flex-col gap-2 p-3">
              <h5 class="text-xl font-medium">{{ item.title }}</h5>
              <p class="text-base text-gray-700">
                {{ item.text }}
              </p>
            </div>
          </div>
        </div>
        <div class="flex justify-center mt-8">
          <button
            class="px-12 py-2 rounded-lg text-green-900 cursor-pointer border border-green-900 hover:text-green-900 hover:bg-green-300 ease-in-out duration-200"
          >
            See full list
          </button>
        </div>
      </div>
    </div>

    <!-- How to use -->
    <div class="w-full h-[820px]" id="how-to-use">
      <div class="w-[86%] mx-auto pb-5">
        <h3 @click="scrollToTop" class="text-4xl font-medium">How to use</h3>
        <div class="relative pt-10">
          <button
            class="absolute left-[42%] top-[50%] flex items-center justify-center p-[12px_20px] rounded bg-[#171A1F] text-white text-lg"
          >
            <p>Watch video</p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="24px"
              viewBox="0 -960 960 960"
              width="24px"
              fill="#FFFFFF"
            >
              <path
                d="M356-252.16v-455.68L707.07-480 356-252.16ZM409-481Zm-1 133 204.77-132L408-612v264Z"
              />
            </svg>
          </button>
          <img src="/assets/images/picV2.png" alt="" />
        </div>
      </div>
    </div>

    <!-- Reviews -->
    <div class="w-full h-[500px]" id="reviews">
      <div class="w-[86%] mx-auto">
        <div class="flex items-center justify-between">
          <h3 @click="scrollToTop" class="text-4xl font-medium">Reviews</h3>
          <button
            class="flex items-center gap-2 px-8 py-[10px] text-base border rounded-md border-green-700"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="18px"
              viewBox="0 -960 960 960"
              width="18px"
              fill="#15803d"
            >
              <path
                d="M96 0v-192h768V0H96Zm168-360h51l279-279-26-27-25-24-279 279v51Zm-72 72v-152.92L594-843q11-11 23.84-16 12.83-5 27-5 14.16 0 27.16 5t24.1 15.94L747-792q11 11 16 24t5 27.4q0 13.49-4.95 26.54-4.95 13.05-15.75 23.85L345-288H192Zm503-455-51-49 51 49ZM594-639l-26-27-25-24 51 51Z"
              />
            </svg>
            Write a review
          </button>
        </div>

        <div class="grid grid-cols-[40%_55%] gap-14 mt-6 py-2">
          <div class="flex flex-col gap-3 pr-8">
            <div class="flex items-center gap-2">
              <div class="text-4xl font-bold">4.5</div>
              <div class="ml-2 text-yellow-500">
                <span v-for="star in 5" :key="star" class="inline-block">
                  <svg
                    v-if="star <= 4.5"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="currentColor"
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                  >
                    <path
                      d="M12 .587l3.668 7.568 8.332 1.151-6.064 5.899 1.428 8.295-7.364-3.868-7.364 3.868 1.428-8.295-6.064-5.899 8.332-1.151z"
                    />
                  </svg>
                  <svg
                    v-else
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    stroke="currentColor"
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M12 2l3.09 6.26L22 9.27l-5 4.87L18.18 21 12 17.27 5.82 21 7 14.14 2 9.27l6.91-1.01L12 2z"
                    />
                  </svg>
                </span>
              </div>
              <div class="ml-2 text-gray-600">368 Reviews</div>
            </div>
            <div
              v-for="(percentage, index) in [60, 25, 10, 5, 0]"
              :key="index"
              class="flex items-center mb-2 gap-2"
            >
              <div class="w-4 text-gray-600">{{ 5 - index }}</div>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                class="w-6 h-6 text-yellow-500"
                viewBox="0 0 24 24"
              >
                <path
                  d="M12 .587l3.668 7.568 8.332 1.151-6.064 5.899 1.428 8.295-7.364-3.868-7.364 3.868 1.428-8.295-6.064-5.899 8.332-1.151z"
                />
              </svg>
              <div class="flex-1 mx-2 bg-gray-200 rounded-full h-2">
                <div
                  :style="{ width: percentage + '%' }"
                  class="h-full bg-yellow-500 rounded-full"
                ></div>
              </div>
              <div class="w-12 text-right text-gray-600">{{ percentage }}%</div>
            </div>
          </div>

          <div class="flex flex-col gap-5">
            <div
              v-for="(person, index) in personals"
              :key="index"
              class="flex flex-col gap-2"
            >
              <div class="flex gap-3">
                <img :src="person.profile" alt="" />
                <div class="flex gap-2">
                  <h4 class="text-sm font-bold">{{ person.name }}</h4>
                  <span class="text-xs text-gray-600"
                    >{{ person.date }}d ago</span
                  >
                </div>
              </div>
              <p class="text-sm">{{ person.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- FAQs -->
    <div class="w-full h-[554px] border" id="faqs">
      <div class="w-[86%] mx-auto py-4">
        <h3 @click="scrollToTop" class="text-4xl font-medium">FAQs</h3>
        
           
      </div>
    </div>
  </div>
</template>

<script setup>
import p1 from "~/assets/images/pic4.png";
import p2 from "~/assets/images/pic5.png";
import p3 from "~/assets/images/pic6.png";
import { personals } from "~/content/allData";
console.log(personals);
const allpic = [
  {
    img: p1,
    title: "Hyaluronic acid",
    text: "Elit do sit excepteur duis labore nisi sit anim adipisicing duis incididunt sit anim sint est exercitation aute consectetur irure",
  },
  {
    img: p2,
    title: "Green tea",
    text: "Tempor adipisicing aute pariatur magna enim Lorem voluptate incididunt culpa ex veniam sunt occaecat tempor ",
  },
  {
    img: p3,
    title: "Olive oil",
    text: "Cupidatat culpa id do laboris nisi aliqua eu. Veniam aliqua duis Lorem adipisicing et minim velit quis ",
  },
];

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};
</script>

