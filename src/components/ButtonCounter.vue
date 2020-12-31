<template>
  <button class="round-button">
    <h1>
      {{ title }}
    </h1>
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
  height: 2em;
  width: 2em;
  border-radius: 50%;
  border: 0;
  background-color: aqua;
  margin: 1em;

  display: flex;
  justify-content: center;
  align-items: center;
  align-self: center;
}

.round-button > span {
  /* display: inline-block;
  vertical-align: middle; */
  max-width: 90%;
}
</style>
