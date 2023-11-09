<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <Menu />
    <input type="text" v-model="name" />
    <section><input type="checkbox" v-model="accept" /> Remember Me</section>
    <section>
      {{ name }}
    </section>
    <Hidden />
    <section>
      <h1
        @click="selected = !selected"
        v-bind:id="id"
        :class="{ selected: selected }"
      >
        {{ id }}
      </h1>
    </section>
    <Model />
    <Todo />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Menu from "@/components/Menu.vue";
import Hidden from "@/components/Hidden.vue";
import Model from "@/components/Model.vue";
import Todo from "@/components/Todo.vue";

export default {
  name: "App",
  data() {
    return {
      name: "Kiril",
      accept: true,
      /* binding id */
      id: 13,
      selected: false,
    };
  },
  components: {
    HelloWorld,
    Menu,
    Hidden,
    Model,
    Todo,
  },
  mounted() {},
  methods: {},
};
</script>

<style scoped>
.selected {
  color: red;
}
</style>
