<template>
  <div class="container">
    <CounterDisplay class="disp" ref="countDisp" />

    <Row class="btns">
      <CounterButton @click="countBtnHandler" title="+" />
      <CounterButton @click="countBtnHandler" title="-" />
    </Row>
  </div>
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
        this.$refs.countDisp.increment();
      } else if (emitValue === "-") {
        // console.log(emitValue);
        this.$refs.countDisp.decrement();
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
  color: #0a0a0a;
  /* margin-top: 60px; */
  height: 100vh;

  background-color: cornflowerblue;
}

/* .btn-row {
  display: flex;
  justify-content: center;
} */

.container {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.disp {
  width: 100%;
  flex: 90%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.btns {
  flex: 10%;
  width: 100%;
  align-items: flex-end;
}
</style>
