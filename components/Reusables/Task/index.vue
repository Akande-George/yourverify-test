<template>
  <div>
    <section class="py-8 border-b border-[#F1F1F1]">
      <div class="flex justify-center space-x-6">
        <div class="">
          <div class="flex justify-center">
            <img src="/icons/add.svg" alt="" />
          </div>
          <div
            class="app-font-medium mt-2 text-[#828282] text-center text-[10px]"
          >
            Assign<br />Agent
          </div>
        </div>
        <div>
          <div class="text-[12px] app-font-medium">{{ name }}</div>
          <div class="text-[12px] text-[#ACB6BE] app-font-medium">
            {{ address }}
          </div>
          <div class="flex justify-start space-x-2">
            <img src="/icons/house.svg" alt="" />
            <div class="text-[12px] text-[#ACB6BE] app-font-medium">
              {{ bank }}
            </div>
          </div>
          <div class="text-[12px] text-[#3056D3] app-font-medium mt-3">
            {{ time }}
          </div>
        </div>
        <div class="flex justify-center items-center">
          <img src="/icons/angle-right.svg" alt="" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: "",
    },
    address: {
      type: String,
      default: "",
    },
    bank: {
      type: String,
      default: "",
    },
    time: {
      type: String,
      default: "",
    },
  },
};
</script>

<style></style>
