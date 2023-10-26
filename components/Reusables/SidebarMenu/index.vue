<template>
  <div>
    <NuxtLink
      :to="menuRoute"
      :class="activeside"
      class="pl-10 py-3 my-4 space-x-5 cursor-pointer hover:bg-primary hover:text-white hover:border-l-4 hover:border-secondary flex justify-start items-center"
    >
      <img :src="`/icons/${menuImg}.svg`" alt="" />
      <div>{{ menu }}</div>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  props: {
    menu: {
      type: String,
      default: "",
    },
    menuImg: {
      type: String,
      default: "",
    },
    activeside: {
      type: String,
      default: "",
    },
  },
};
</script>

<style scoped>
.activeSidebar {
  color: white;
  border-left: 4px solid #115766;
  background-color: #46b2c8;
}
</style>
