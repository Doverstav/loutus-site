<template>
  <div id="app">
    <NavBar/>
    <DoubleGradient />
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import DoubleGradient from "./components/DoubleGradientContainer";

export default {
  name: "App",
  components: {
    NavBar,
    DoubleGradient
  }
};
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: lightgray;
  min-height: 100vh;

  overflow-x: hidden;
}
</style>
