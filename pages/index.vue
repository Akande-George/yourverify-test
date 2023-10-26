<template>
  <div class="pageContainer h-full w-[100%]">
    <section class="lg:flex lg:justify-between">
      <div class="w-[392px]">
        <Tasks />
      </div>
      <div class="w-[392px]">
        <Agents />
      </div>
    </section>
  </div>
</template>

<script>
import Tasks from "~/components/Tasks";
import Agents from "~/components/Agents";
export default {
  components: {
    Tasks,
    Agents,
  },
};
</script>

<style scoped>
.pageContainer {
  width: 100%;
  height: 100%;
  background-image: url("/images/map.png");
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
