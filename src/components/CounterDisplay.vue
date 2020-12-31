<template>
  <div class="countdown">
    {{ count }}
  </div>
</template>

<script>
export default {
  name: "CounterDisplay",
  data: function() {
    return {
      count: 0
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decremenr() {
      this.count--;
    }
  }
};
</script>

<style scoped>
.countdown {
  display: flex;
  justify-content: center;
  align-content: center;

  font-size: 2em;
}
</style>
