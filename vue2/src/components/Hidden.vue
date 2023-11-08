<template>
  <section>
    <section v-show="isShow">
      <h1>Display</h1>
    </section>
    <button @click="isShow = !isShow">Hidden</button>
  </section>
</template>

<script>
export default {
  name: "Hidden",
  data() {
    return {
      isShow: true,
    };
  },
};
</script>
