<template>
  <div>
    <div>
      <SidebarHeader />
    </div>
    <div class="pt-6">
      <div v-for="menu in menuList" :key="menu.index">
        <SidebarMenu
          :menu="menu.menu"
          :menuImg="menu.menuImg"
          :menuRoute="menu.route"
          :activeside="menu.className"
        />
      </div>
    </div>
  </div>
</template>

<script>
import SidebarHeader from "~/components/Reusables/SidebarHeader";
import SidebarMenu from "~/components/Reusables/SidebarMenu";
export default {
  components: {
    SidebarHeader,
    SidebarMenu,
  },
  data() {
    return {
      menuList: [
        {
          menuImg: "Work",
          menu: "Dashboard",
          route: "/",
          className: "activeSidebar",
        },
        {
          menuImg: "agents",
          menu: "Agents",
          route: "/agents",
          className: "",
        },
        {
          menuImg: "task",
          menu: "Task",
          route: "/task",
          className: "",
        },
        {
          menuImg: "users",
          menu: "Users",
          route: "/users",
          className: "",
        },
        {
          menuImg: "Setting",
          menu: "Settings",
          route: "/settings",
          className: "",
        },
      ],
    };
  },
};
</script>

<style></style>
