<template>
  <section class="todoitem">
    <input type="checkbox" v-model="taskData.done" />
    <span :class="{ done: taskData.done }">
      {{ taskData.todo }}
    </span>
  </section>
</template>

<script>
export default {
  name: "ToDoItem",
  props: ["taskData"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.done {
  color: #8e8e8e;
}
</style>
