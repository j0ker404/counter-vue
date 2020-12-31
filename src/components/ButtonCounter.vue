<template>
  <button class="round-button">
    {{ title }}
    <!-- <span>
    </span> -->
  </button>
</template>

<script>
export default {
  name: "CounterButton",
  props: ["title"],
};
</script>

<style scoped>
/* 
https://stackoverflow.com/questions/37373734/fully-circular-buttons-with-dynamic-size
 */
.round-button {
  /* make circular */
  height: 2em;
  width: 2em;
  border-radius: 50%;
  border: 0;
  background-color: aqua;
  margin: 1em;

  /* center text */
  display: flex;
  justify-content: center;
  align-items: center;

  font: 2em sans-serif;
}
</style>
