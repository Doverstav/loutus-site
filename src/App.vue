<template>
  <div id="app">
    <!--img alt="Vue logo" src="./assets/logo.png"-->
    <!--HelloWorld msg="Welcome to Your Vue.js App"/-->
    <BoxContainer />
    <BigText />
  </div>
</template>

<script>
import BoxContainer from "./components/BoxContainer";
import BigText from "./components/BigText";

export default {
  name: "App",
  components: {
    BoxContainer,
    BigText
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  overflow-x: hidden;
}
</style>
