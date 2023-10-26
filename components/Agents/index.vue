<template>
  <div>
    <section class="flex justify-end">
      <button
        class="w-[10%] bg-black p-2 h-[48px]"
        @click="showTask = !showTask"
      >
        <img v-if="showTask" src="/icons/white-right-arrow.svg" alt="" />
        <img v-else src="/icons/white-left-arrow.svg" alt="" />
      </button>
      <div class="w-[90%]" v-if="showTask">
        <div class="px-4 py-3 bg-primary flex justify-between items-center">
          <div class="text-white app-font-semibold">Agents</div>
          <div>
            <img src="/icons/white-search.svg" alt="" />
          </div>
        </div>
        <div class="bg-white">
          <div
            class="flex justify-between text-[14px] text-[#C4C4C4] border-b border-[#F1F1F1]"
          >
            <button
              @click="unassignedAction"
              :class="activeUnassigned"
              class="py-4 px-8 app-font-medium"
            >
              All
            </button>
            <button
              @click="assignedAction"
              :class="activeAssigned"
              class="py-4 px-8 app-font-medium flex justify-between space-x-3 items-center"
            >
              <img src="/icons/green-dot.svg" alt="" />
              <div>Online</div>
            </button>
            <button
              @click="completedAssigned"
              :class="activeCompleted"
              class="py-4 px-8 app-font-medium flex justify-between space-x-3 items-center"
            >
              <img src="/icons/red-dot.svg" alt="" />
              <div>Offline</div>
            </button>
          </div>
          <div class="md:h-screen overflow-y-auto">
            <div v-for="agent in agents" :key="agent.index">
              <Agent
                :name="agent.name"
                :location="agent.location"
                :avatar="agent.avatar"
                :phone="agent.phone"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Agent from "~/components/Reusables/Agent";
export default {
  components: {
    Agent,
  },
  data() {
    return {
      showTask: true,
      activeUnassigned: "",
      activeAssigned: "",
      activeCompleted: "",
      agents: [
        {
          avatar: "avatar1",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
        {
          avatar: "b",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
        {
          avatar: "c",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
        {
          avatar: "b",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
        {
          avatar: "c",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
        {
          avatar: "d",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
        {
          avatar: "e",
          name: "Adebayo Adeoye Emmanuel",
          phone: "08069786754",
          location: "Akure",
        },
      ],
    };
  },
  methods: {
    unassignedAction() {
      this.activeUnassigned = "active";
      this.activeAssigned = "";
      this.activeCompleted = "";
    },
    assignedAction() {
      this.activeUnassigned = "";
      this.activeAssigned = "active";
      this.activeCompleted = "";
    },
    completedAssigned() {
      this.activeUnassigned = "";
      this.activeAssigned = "";
      this.activeCompleted = "active";
    },
  },
  mounted() {
    this.unassignedAction();
  },
};
</script>

<style scoped>
.active {
  color: #023a59;
  border-bottom: #023a59 solid;
}
</style>
