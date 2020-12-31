<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <CounterDisplay />
  <!-- <div class="btn-row">
  </div> -->

  <Row>
    <CounterButton title="+" />
    <CounterButton title="-" />
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
