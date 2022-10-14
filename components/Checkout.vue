<!-- Please remove this file from your project -->
<template>
  <div style="background-color: #f5f5f5">
    <img src="~/assets/Checkout.png" />
    <div class="w-2/3 mx-auto mt-2 mb-2">
      <div
        class="flex justify-between items-center bg-white ml-6 mr-8 p-4 text-black"
        style="font-size: 16px"
      >
        <div class="flex items-center">
          <img class="h-5" src="~/assets/invest-1.png" />
          <p class="pl-2">Invest Round Up</p>
          <div class="mx-6 font-medium" style="font-size: 13px; color: #929292">
            A round up of value of RM1 will be invested to ASNB fund
          </div>
        </div>

        <div
          class="relative inline-block w-10 mr-2 align-middle select-none transition duration-200 ease-in"
        >
          <input
            v-model="checked"
            type="checkbox"
            name="toggle"
            id="toggle"
            class="toggle-checkbox absolute block w-6 h-6 rounded-full bg-white border-4 appearance-none cursor-pointer"
          />
          <label
            for="toggle"
            class="toggle-label block overflow-hidden h-6 rounded-full bg-gray-300 cursor-pointer"
          ></label>
        </div>
      </div>

      <!-- Toggle On Component -->
      <div
        v-if="checked"
        class="flex justify-between items-center bg-white ml-6 mr-8 py-4 px-8 text-black border-t"
        style="font-size: 16px"
      >
        <div class="flex w-3/5">
          <div class="whitespace-nowrap flex flex-col justify-end items-end">
            <p v-if="!signedUp" class="py-1 mb-3">ASNB Account Number</p>
            <p class="py-1">Round up value</p>
          </div>
          <div class="">
            <input
              v-if="!signedUp"
              class="rounded mx-8 mb-3 w-64 text-gray-700 bg-white border border-solid border-gray-300 transition ease-in-out focus:text-gray-700 focus:bg-white text-xs px-2 py-1"
              placeholder="Enter your ASNB Account Number"
            />
            <div
              class="relative mt-1 bg-white border border-solid border-gray-300 mx-8 w-64 rounded"
            >
              <div
                class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-2"
              >
                <span class="text-gray-400 text-xs">RM</span>
              </div>
              <input
                type="text"
                name="price"
                id="price"
                v-model="price"
                class="block w-full rounded-md border-gray-300 px-10 text-black"
              />
            </div>
          </div>
        </div>
        <div class="w-2/5 self-end flex justify-end">
          <div v-if="!signedUp" class="justify-self-end">
            <button @click="signedUp = true" class="w-full text-white">toggle</button>
            <p class="text-gray-500 text-xs">Have not signed up?</p>
            <button
              class="text-white px-4 py-1 rounded mt-1"
              style="background-color: #1c5195"
            >
              Create an ASNB Account
            </button>
          </div>
        </div>
      </div>
    </div>
    <img src="~/assets/Checkout3.png" />
    <img src="~/assets/Checkout2.png" />
  </div>
</template>

<script>
export default {
  name: "Checkout",
  data() {
    return {
      checked: false,
      signedUp: false,
      price: '1.00'
    }
  }
};
</script>

<style>
.toggle-checkbox:checked {
  right: 0;
  border-color: #ee4d2d;
}
.toggle-checkbox:checked + .toggle-label {
  background-color: #ee4d2d;
}
</style>
