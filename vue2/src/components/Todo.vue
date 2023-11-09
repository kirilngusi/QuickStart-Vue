<template>
  <div>
    <input type="text" v-model="newTask" />
    <button @click="addTask()">Add</button>
    <ToDoItem v-for="(task, index) in tasks" :key="index" :taskData="task" />
  </div>
</template>

<script>
import ToDoItem from "@/components/ToDoItem.vue";

export default {
  name: "Todo",
  data() {
    return {
      newTask: "",
      tasks: [
        { todo: "sleep", done: false },
        { todo: "sleep2 sleep", done: false },
        { todo: "sleep3 sleep", done: true },
      ],
    };
  },
  components: {
    ToDoItem,
  },

  // handle data
  methods: {
    addTask: () => {
      this.tasks.push({ todo: this.newTask, done: false });
    },
  },

  watch: {
    newTask: (oldValue, newValue) => {
      console.log("oldValue", oldValue);
      console.log("new task changed");
      console.log("newValue", newValue);
    },
  },
  async mounted() {
    try {
      // call api
    } catch (e) {
      console.log(e);
    }
  },
};
</script>
