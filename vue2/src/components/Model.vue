<template>
  <section>
    <form action="/abc">
      <input ref="channelName" type="text" v-model="channel.name" />
      <button type="submit" @click.prevent="channel.name = 'abc'">Click</button>
    </form>
  </section>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {
      channel: {
        name: "KirilSilly",
      },
    };
  },
  mounted() {
    console.log(this.channel.name);
  },
  methods: {},
};
</script>
