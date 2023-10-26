<template>
  <div>
    <section class="py-8 border-b border-[#F1F1F1]">
      <div class="flex justify-center space-x-6">
        <div class="">
          <img class="rounded-full" :src="`/images/${avatar}.png`" alt="" />
        </div>
        <div>
          <div class="text-[12px] app-font-medium">{{ name }}</div>
          <div class="text-[12px] text-[#ACB6BE] app-font-medium">
            {{ phone }}
          </div>
          <div class="flex justify-start space-x-2">
            <div class="text-[12px] text-[#ACB6BE] app-font-medium">
              {{ location }}
            </div>
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
    avatar: {
      type: String,
      default: "",
    },
    name: {
      type: String,
      default: "",
    },
    phone: {
      type: String,
      default: "",
    },
    location: {
      type: String,
      default: "",
    },
  },
};
</script>

<style></style>
