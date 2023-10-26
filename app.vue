<template>
  <section>
    <div class="fixed bg-white w-full">
      <AppHeader @toggleSidebar="showSidebar = !showSidebar" />
    </div>
    <section class="flex flex-wrap lg:flex-nowrap pt-20">
      <aside
        v-if="showSidebar"
        id="sidebar"
        class="block bg-white w-full md:w-[257px] transition duration-1000 ease-in-out"
      >
        <Sidebar />
      </aside>
      <div class="pt-6 lg:flex-1">
        <section class="border-l border-[#F1F1F1] overflow-y-auto h-screen">
          <NuxtPage />
        </section>
      </div>
    </section>
  </section>
</template>

<script>
import AppHeader from "~/components/AppHeader";
import Sidebar from "~/components/Sidebar";
export default {
  components: {
    AppHeader,
    Sidebar,
  },
  data() {
    return {
      showSidebar: true,
    };
  },
};
</script>

<style scoped>
@media only screen and (max-device-width: 812px) {
  #sidebar {
    z-index: 100;
    height: 100vh;
    position: fixed;
  }
}
</style>
