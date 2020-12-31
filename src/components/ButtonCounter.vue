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
    },
  },
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

  /* 
    https://codepen.io/seme332/pen/reJOwo  
  */
  background-color: #fff;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
  cursor: pointer;
  /*
    animation effect
    see hover for transform
   */
  transition: all 0.3s ease 0s;
}

.round-button:hover {
  /* background-color: #2ee59d; */
  /* color: #fff; */
  box-shadow: 0px 15px 20px rgba(0, 0, 0, 0.1);
  transform: translateY(-7px);
}
</style>
