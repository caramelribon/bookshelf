<template>
  <button v-on:click="countUp">
    {{ count }} すごいね！
  </button>
</template>

<script>
export default {
  data() {
    return { count: 0 };
  },
  methods: {
    countUp() {
      this.count += 1;
    },
  },
};
</script>
