<template>
  <button class="round-button" v-on:click="btnEmitter">
    {{ title }}
  </button>
</template>

<script>
export default {
  name: "CounterButton",
  // [title] is displayed on btn
  props: ["title"],
  emits: ["click"],

  methods: {
    btnEmitter(event) {
      // button event trigger function
      this.$emit("click", this.title);
      // console.log(event);
      if (event) {
        event.preventDefault();
      }
    }
  }
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
