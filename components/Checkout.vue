<!-- Please remove this file from your project -->
<template>
  <div style="background-color: #f5f5f5">
    <img src="~/assets/Checkout.png" />
    <div class="w-2/3 mx-auto mt-2 mb-2">
      <div class="flex justify-between items-center bg-white ml-6 mr-8 p-4 text-black" style="font-size: 16px">
        <div class="flex items-center">
          <img class="h-5" src="~/assets/invest-1.png" />
          <p class="pl-2">Invest Round Up</p>
          <div class="mx-6 font-medium" style="font-size: 13px; color: #929292">
            A round up of value of RM1 will be invested to ASNB fund
          </div>
        </div>

        <input type="checkbox" value="" id="default-toggle" class="sr-only peer" />
        <div class="form-check form-switch justify-self-end">
          <input
            class="form-check-input appearance-none w-9 -ml-10 rounded-full float-left h-5 align-top bg-no-repeat bg-contain bg-gray-300 focus:outline-none focus:bg-red-400 cursor-pointer shadow-sm"
            type="checkbox" role="switch">
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
};
</script>
