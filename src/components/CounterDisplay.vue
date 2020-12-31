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
      // increment count value
      this.count++;
    },
    decrement() {
      // increment count value
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

  font-size: 10em;
}
</style>
