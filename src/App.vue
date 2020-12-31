<template>
  <CounterDisplay ref="countDisp"/>

  <Row>
    <CounterButton  @click="countBtnHandler" title="+" />
    <CounterButton  @click="countBtnHandler" title="-" />
  </Row>
</template>

<script>
import CounterDisplay from "./components/CounterDisplay";
import CounterButton from "./components/ButtonCounter";
import Row from "./components/Row";

export default {
  name: "App",
  components: {
    CounterDisplay,
    CounterButton,
    Row,
  },
  methods: {
    countBtnHandler(emitValue) {
      // call displayCounter
      // increment/decrement method
      // based on emitValue
      
      if (emitValue === "+") {
        // console.log(emitValue);
        this.$refs.countDisp.increment()
      } else if (emitValue === "-") {
        // console.log(emitValue);
        this.$refs.countDisp.decrement()
      }
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  height: 100vh;
}

/* .btn-row {
  display: flex;
  justify-content: center;
} */
</style>
