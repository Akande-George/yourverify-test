<template>
  <div>
    <section class="flex">
      <div class="w-[90%]" v-if="showTask">
        <div class="px-4 py-3 bg-primary text-white app-font-semibold">
          Task
        </div>
        <div class="bg-white">
          <div
            class="flex justify-between text-[14px] text-[#C4C4C4] border-b border-[#F1F1F1]"
          >
            <button
              @click="unassignedAction"
              :class="activeUnassigned"
              class="py-4 px-2 app-font-medium"
            >
              24 Unassigned
            </button>
            <button
              @click="assignedAction"
              :class="activeAssigned"
              class="py-4 px-2 app-font-medium"
            >
              12 Assigned
            </button>
            <button
              @click="completedAssigned"
              :class="activeCompleted"
              class="py-4 px-2 app-font-medium"
            >
              30 Completed
            </button>
          </div>
          <div class="lg:h-screen overflow-y-auto">
            <div v-for="task in tasks" :key="task.index">
              <Task
                :name="task.name"
                :address="task.address"
                :bank="task.bank"
                :time="task.time"
              />
            </div>
          </div>
        </div>
      </div>
      <button
        class="w-[10%] bg-black p-2 h-[48px]"
        @click="showTask = !showTask"
      >
        <img v-if="showTask" src="/icons/white-left-arrow.svg" alt="" />
        <img v-else src="/icons/white-right-arrow.svg" alt="" />
      </button>
    </section>
  </div>
</template>

<script>
import Task from "~/components/Reusables/Task";
export default {
  components: {
    Task,
  },
  data() {
    return {
      showTask: true,
      activeUnassigned: "",
      activeAssigned: "",
      activeCompleted: "",
      tasks: [
        {
          name: "Abiodun Olawale Solomon",
          address: "12b Emmanuel Hign street, Sur...",
          bank: "Sterling Bank PLC",
          time: "A Day Ago",
        },
        {
          name: "Abiodun Olawale Solomon",
          address: "12b Emmanuel Hign street, Sur...",
          bank: "Sterling Bank PLC",
          time: "2 Days Ago",
        },
        {
          name: "Abiodun Olawale Solomon",
          address: "12b Emmanuel Hign street, Sur...",
          bank: "Sterling Bank PLC",
          time: "3 Days Ago",
        },
        {
          name: "Abiodun Olawale Solomon",
          address: "12b Emmanuel Hign street, Sur...",
          bank: "Sterling Bank PLC",
          time: "4 Days Ago",
        },
        {
          name: "Abiodun Olawale Solomon",
          address: "12b Emmanuel Hign street, Sur...",
          bank: "Sterling Bank PLC",
          time: "4 Days Ago",
        },
        {
          name: "Abiodun Olawale Solomon",
          address: "12b Emmanuel Hign street, Sur...",
          bank: "Sterling Bank PLC",
          time: "4 Days Ago",
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
