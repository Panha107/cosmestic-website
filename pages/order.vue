<template>
  <div>
    <div class="w-full h-[1100px]">
      <div class="w-[86%] mx-auto pt-12">
        <h3 class="text-4xl font-sans font-bold flex justify-center">
          My Shopping Bag (3 Items)
        </h3>
        <div class="grid grid-cols-[70%_30%] gap-2 mt-16">
          <!--main -->
          <div class="flex flex-col gap-3">
            <div class="border p-4 rounded-md">
              <div class="flex items-center gap-3">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  height="20px"
                  viewBox="0 -960 960 960"
                  width="20px"
                  fill="#000000"
                >
                  <path
                    d="M263.79-96Q234-96 213-117.21t-21-51Q192-198 213.21-219t51-21Q294-240 315-218.79t21 51Q336-138 314.79-117t-51 21Zm432 0Q666-96 645-117.21t-21-51Q624-198 645.21-219t51-21Q726-240 747-218.79t21 51Q768-138 746.79-117t-51 21ZM253-696l83 192h301l82-192H253Zm-31-72h570q14 0 20.5 11t1.5 23L702.63-476.14Q694-456 676.5-444T637-432H317l-42 72h493v72H276q-43 0-63.5-36.15-20.5-36.16.5-71.85l52-90-131-306H48v-72h133l41 96Zm114 264h301-301Z"
                  />
                </svg>
                <span class="text-xl font-medium">Order Summary</span>
              </div>
              <div class="w-full">
                <div class="flex justify-between items-center">
                  <span>Name</span>
                  <div class="w-[55%] flex justify-around py-2">
                    <span>Price</span>
                    <span>Quantity</span>
                    <span>Total</span>
                    <span></span>
                  </div>
                </div>
              </div>
              <div class="flex flex-col gap-3">
                <div
                  v-for="(item, index) in products.slice(0, 2)"
                  :key="index"
                  class="flex justify-between items-center border-b"
                >
                  <img class="w[65px] h-[77px]" :src="item.img" alt="" />
                  <div>
                    <p class="text-sm">Product name</p>
                    <select
                      class="border rounded pl-2 px-9 text-gray-400"
                      id="size"
                    >
                      <option value="50">50ML</option>
                    </select>
                  </div>
                  <div class="w-[55%] flex justify-around py-2">
                    <span>{{ item.price }}</span>
                    <div class="flex items-center gap-2">
                      <button class="text-lg px-2 border rounded">-</button>
                      <span>1</span>
                      <button class="text-lg px-2 border rounded">+</button>
                    </div>
                    <span>1</span>
                    <button class="">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        height="20px"
                        viewBox="0 -960 960 960"
                        width="20px"
                        fill="#5f6368"
                      >
                        <path
                          d="M280-120q-33 0-56.5-23.5T200-200v-520h-40v-80h200v-40h240v40h200v80h-40v520q0 33-23.5 56.5T680-120H280Zm400-600H280v520h400v-520ZM360-280h80v-360h-80v360Zm160 0h80v-360h-80v360ZM280-720v520-520Z"
                        />
                      </svg>
                    </button>
                  </div>
                </div>
              </div>
            </div>
            <!--  -->
            <div class="flex flex-col gap-3 border p-4 rounded-md">
              <div class="flex flex-col gap-3">
                <div class="flex items-center gap-2">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    height="24px"
                    viewBox="0 -960 960 960"
                    width="24px"
                    fill="#5f6368"
                  >
                    <path
                      d="M240-160q-50 0-85-35t-35-85H40v-440q0-33 23.5-56.5T120-800h560v160h120l120 160v200h-80q0 50-35 85t-85 35q-50 0-85-35t-35-85H360q0 50-35 85t-85 35Zm0-80q17 0 28.5-11.5T280-280q0-17-11.5-28.5T240-320q-17 0-28.5 11.5T200-280q0 17 11.5 28.5T240-240ZM120-360h32q17-18 39-29t49-11q27 0 49 11t39 29h272v-360H120v360Zm600 120q17 0 28.5-11.5T760-280q0-17-11.5-28.5T720-320q-17 0-28.5 11.5T680-280q0 17 11.5 28.5T720-240Zm-40-200h170l-90-120h-80v120ZM360-540Z"
                    />
                  </svg>
                  <span class="text-xl font-medium">Delivery Options</span>
                </div>
                <div class="flex flex-col gap-1">
                  <span class="text-base font-semibold">Operator</span>
                  <div class="flex gap-4 *:flex *:gap-2">
                    <div>
                      <input id="ups" name="operator" type="radio" />
                      <label for="ups">UPS</label>
                    </div>
                    <div>
                      <input id="fedex" name="operator" type="radio" />
                      <label for="fedex">FedEx</label>
                    </div>
                    <div>
                      <input id="dhl" name="operator" type="radio" />
                      <label for="dhl">DHL</label>
                    </div>
                  </div>
                </div>
                <div class="grid grid-cols-2 gap-6">
                  <div class="border rounded-md p-3 bg-green-50">
                    <div class="flex gap-2 *:text-[#459D7A]">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        height="20px"
                        viewBox="0 -960 960 960"
                        width="20px"
                        fill="#459D7A"
                      >
                        <path
                          d="m429-336 238-237-51-51-187 186-85-84-51 51 136 135Zm51 240q-79 0-149-30t-122.5-82.5Q156-261 126-331T96-480q0-80 30-149.5t82.5-122Q261-804 331-834t149-30q80 0 149.5 30t122 82.5Q804-699 834-629.5T864-480q0 79-30 149t-82.5 122.5Q699-156 629.5-126T480-96Zm0-72q130 0 221-91t91-221q0-130-91-221t-221-91q-130 0-221 91t-91 221q0 130 91 221t221 91Zm0-312Z"
                        />
                      </svg>
                      <div class="flex flex-col">
                        <span class="text-xl font-bold">$22</span>
                        <span> Instant delivery </span>
                        <span>Est. arrival: Today</span>
                      </div>
                    </div>
                  </div>

                  <div class="border rounded-md p-3">
                    <div class="flex gap-2 *:text-[#171A1F]">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        height="20px"
                        viewBox="0 -960 960 960"
                        width="20px"
                        fill="#9095A0"
                      >
                        <path
                          d="m429-336 238-237-51-51-187 186-85-84-51 51 136 135Zm51 240q-79 0-149-30t-122.5-82.5Q156-261 126-331T96-480q0-80 30-149.5t82.5-122Q261-804 331-834t149-30q80 0 149.5 30t122 82.5Q804-699 834-629.5T864-480q0 79-30 149t-82.5 122.5Q699-156 629.5-126T480-96Zm0-72q130 0 221-91t91-221q0-130-91-221t-221-91q-130 0-221 91t-91 221q0 130 91 221t221 91Zm0-312Z"
                        />
                      </svg>
                      <div class="flex flex-col">
                        <span class="text-xl font-bold">$12</span>
                        <span> Standard delivery </span>
                        <span>Est. arrival: DD/MM</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="flex flex-col gap-3 border p-4 rounded-md">
              <div class="flex flex-col gap-3">
                <div class="flex items-center gap-2">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    height="24px"
                    viewBox="0 -960 960 960"
                    width="24px"
                    fill="#666666"
                  >
                    <path
                      d="M234-276q51-39 114-61.5T480-360q69 0 132 22.5T726-276q35-41 54.5-93T800-480q0-133-93.5-226.5T480-800q-133 0-226.5 93.5T160-480q0 59 19.5 111t54.5 93Zm246-164q-59 0-99.5-40.5T340-580q0-59 40.5-99.5T480-720q59 0 99.5 40.5T620-580q0 59-40.5 99.5T480-440Zm0 360q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-80q53 0 100-15.5t86-44.5q-39-29-86-44.5T480-280q-53 0-100 15.5T294-220q39 29 86 44.5T480-160Zm0-360q26 0 43-17t17-43q0-26-17-43t-43-17q-26 0-43 17t-17 43q0 26 17 43t43 17Zm0-60Zm0 360Z"
                    />
                  </svg>
                  <span class="text-xl font-medium">Customer Information</span>
                </div>
                <!-- <form> -->
                <div class="flex gap-4">
                  <div class="flex flex-col w-[50%] gap-1 *:text-sm">
                    <label class="font-bold" for="">Full name</label>
                    <input
                      class="border pl-3 py-1 bg-gray-100 rounded-md"
                      type="text"
                      placeholder="Amaya Dunne"
                    />
                  </div>
                  <div class="w-[50%] flex flex-col gap-1 *:text-sm">
                    <label class="font-bold" for="">Phone number</label>
                    <input
                      class="border pl-3 py-1 bg-gray-100 rounded-md"
                      type="text"
                      placeholder="732-123-4567"
                    />
                  </div>
                </div>
                <div class="flex flex-col gap-1 *:text-sm">
                  <label class="font-bold" for="">Address</label>
                  <input
                    class="border pl-3 py-1 bg-gray-100 rounded-md focus:outline-none"
                    type="text"
                    placeholder="4706 Pooz Street, Bayville, New Jersey(NJ)"
                  />
                </div>
                <div class="flex gap-2 items-center *:text-sm">
                  <input id="save" type="checkbox" />
                  <label for="save">Save as default</label>
                </div>
                <div
                  class="border p-4 flex gap-6 items-center bg-red-50 rounded"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    height="18px"
                    viewBox="0 -960 960 960"
                    width="18px"
                    fill="#D16D6A"
                  >
                    <path
                      d="M480-280q17 0 28.5-11.5T520-320q0-17-11.5-28.5T480-360q-17 0-28.5 11.5T440-320q0 17 11.5 28.5T480-280Zm-40-160h80v-240h-80v240Zm40 360q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-80q134 0 227-93t93-227q0-134-93-227t-227-93q-134 0-227 93t-93 227q0 134 93 227t227 93Zm0-320Z"
                    />
                  </svg>
                  <div class="flex flex-col gap-2 *:text-xs">
                    <label for="deliverynote" class="font-semibold"
                      >Delivery note</label
                    >
                    <span
                      >Eiusmod et nisi non sunt dolor proident consequat irure
                      ut exercitation consectetur fugiat</span
                    >
                  </div>
                </div>
                <!-- </form> -->
              </div>
            </div>
          </div>

          <div class="h-fit flex flex-col gap-3 pl-6 p-4 border rounded-md">
            <span class="text-2xl font-medium">Payment Method</span>
            <div class="flex flex-col gap-2 *:text-xs">
              <label for="ehange" class="text-blue-600"
                >Change payment methods</label
              >
              <div
                class="flex items-center justify-between p-2 py-3 pl-4 border rounded-md bg-green-100 *:text-green-800"
              >
                <div class="flex items-center gap-2">
                  <img
                    class="w-7 h-7"
                    src="/assets/images/masterCard.svg"
                    alt=""
                  />
                  <span>Mastercard</span>
                </div>
                <span>**** 5987</span>
              </div>
            </div>
            <div class="flex flex-col gap-2 pt-12">
              <div class="w-full flex gap-3 *:text-sm">
                <input
                  class="w-[80%] pl-3 p-2 border rounded-md focus:outline-none"
                  type="text"
                  placeholder="code discount"
                />
                <button class="p-2 px-3 rounded-md bg-green-100">Apply</button>
              </div>
              <span
                class="w-fit text-xs text-orange-400 p-1 bg-orange-200 rounded-xl"
                >15$ OFF</span
              >
            </div>
            <div class="flex flex-col gap-3 pt-8">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#7A2917"
              >
                <path
                  d="M240-80q-50 0-85-35t-35-85v-120h120v-560l60 60 60-60 60 60 60-60 60 60 60-60 60 60 60-60 60 60 60-60v680q0 50-35 85t-85 35H240Zm480-80q17 0 28.5-11.5T760-200v-560H320v440h360v120q0 17 11.5 28.5T720-160ZM360-600v-80h240v80H360Zm0 120v-80h240v80H360Zm320-120q-17 0-28.5-11.5T640-640q0-17 11.5-28.5T680-680q17 0 28.5 11.5T720-640q0 17-11.5 28.5T680-600Zm0 120q-17 0-28.5-11.5T640-520q0-17 11.5-28.5T680-560q17 0 28.5 11.5T720-520q0 17-11.5 28.5T680-480ZM240-160h360v-80H200v40q0 17 11.5 28.5T240-160Zm-40 0v-80 80Z"
                />
              </svg>
              <div
                class="flex flex-col gap-2 *:text-sm *:flex *:justify-between"
              >
                <div class="">
                  Subtotal <span class="font-medium">$180</span>
                </div>
                <div class="">
                  Discount <span class="font-medium">-$15</span>
                </div>
                <div class="">
                  Deliverry Fee <span class="font-medium">$22</span>
                </div>
                <div class="border-t my-3"></div>
                <div>
                  Total
                  <span class="text-xl font-semibold text-orange-600"
                    >$187</span
                  >
                </div>
              </div>
            </div>
            <NuxtLink
              to="/Purchases/purchaseSuccess"
              class="flex justify-center text-lg text-white py-3 bg-green-600 rounded-lg my-2"
              >Proceed to payment</NuxtLink
            >
          </div>
        </div>
      </div>
    </div>
    <div class="w-full h-[600px]">
      <div class="w-[86%] mx-auto">
        <span class=" text-4xl font-semibold">Related products</span>
        <product-4 class="pt-11" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { products } from "~/content/allData";
import Product4 from "~/components/Product4.vue";
</script>
<!-- <template>
  <div class="bg-white p-4">
    <h2 class="text-lg font-semibold">Order Summary</h2>
    <div
      v-for="(item, index) in items"
      :key="index"
      class="flex items-center py-2 border-b"
    >
      <img :src="item.image" alt="" class="h-12 w-12 object-cover" />
      <div class="ml-4 flex-grow">
        <p>{{ item.name }}</p>
        <select class="form-select mt-1 block w-full border-gray-300">
          <option v-for="size in item.sizes" :key="size" :value="size">
            {{ size }}
          </option>
        </select>
      </div>
      <p class="mx-4">{{ item.price }}</p>
      <div class="flex items-center">
        <button @click="decrementQuantity(index)" class="px-2">-</button>
        <p class="mx-2">{{ item.quantity }}</p>
        <button @click="incrementQuantity(index)" class="px-2">+</button>
      </div>
      <p class="mx-4">{{ item.total }}</p>
      <button @click="removeItem(index)" class="text-red-500">🗑️</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          image: "path/to/image1.jpg",
          name: "Product 1",
          sizes: ["S", "M", "L"],
          price: "$10.00",
          quantity: 1,
          total: "$10.00",
        },
        {
          image: "path/to/image2.jpg",
          name: "Product 2",
          sizes: ["S", "M", "L"],
          price: "$15.00",
          quantity: 1,
          total: "$15.00",
        },
      ],
    };
  },
  methods: {
    incrementQuantity(index) {
      this.items[index].quantity++;
      this.updateTotal(index);
    },
    decrementQuantity(index) {
      if (this.items[index].quantity > 1) {
        this.items[index].quantity--;
        this.updateTotal(index);
      }
    },
    updateTotal(index) {
      const item = this.items[index];
      item.total = `$${(item.price.slice(1) * item.quantity).toFixed(2)}`;
    },
    removeItem(index) {
      this.items.splice(index, 1);
    },
  },
};
</script> -->
