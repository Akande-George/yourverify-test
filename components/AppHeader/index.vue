<template>
  <div class="py-2 px-2 lg:px-6 border-b-2 border-[#f5f2f2]">
    <div class="flex justify-start">
      <img src="/images/logo.svg" alt="" />
      <div class="flex justify-end lg:justify-start space-x-3">
        <div class="py-4 pl-10">
          <div
            @click="toggleSidebar"
            class="rounded-full arrow-circle flex justify-center p-1 w-[32px] h-[32px] bg-white shadow-md"
          >
            <img v-if="arrow" src="/icons/right-arrow.svg" alt="" />
            <img v-else src="/icons/left-arrow.svg" alt="" />
          </div>
        </div>
        <div class="hidden lg:block">
          <Search />
        </div>
        <!-- <div class="block lg:hidden">
            <img src="/icons/Search.svg" alt="">
        </div> -->
        <div
          class="p-2 flex justify-between lg:justify-between space-x-3 md:space-x-6"
        >
          <div
            class="p-3 w-[48px] h-[48px] rounded-[12px] bg-[#f3fdff] py-3 hidden lg:block"
          >
            <img src="/icons/Notification.svg" alt="" />
          </div>
          <div class="py-1">
            <img class="rounded-full" src="/images/avatar1.png" alt="" />
          </div>
          <div class="py-3 hidden lg:block">Solomon</div>
          <div class="py-3">
            <img src="/icons/primary-down-arrow.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Search from "./search.vue";
export default {
  components: {
    Search,
  },
  data() {
    return {
      arrow: true,
    };
  },
  methods: {
    toggleSidebar() {
      this.$emit("toggleSidebar");
      this.arrow = !this.arrow;
    },
  },
};
</script>

<style scoped>
.arrow-circle {
  filter: drop-shadow(0px 2px 4px rgba(2, 58, 89, 0.16));
}
</style>
