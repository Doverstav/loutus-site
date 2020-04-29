<template>
  <div id="app">
    <!-- 
      TODO: Create top level div that handles sizing of navbar and main content
      insteadof each component handling it separately
    -->
    <NavBar/>
    <MainContent />
  </div>
</template>

<script>
import NavBar from "./components/nav/NavBar";
import MainContent from "./components/pages/MainContent";

export default {
  name: "App",
  components: {
    NavBar,
    MainContent
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
  background-color: #EAEAEA;
  min-height: 100vh;

  display: grid;
  grid-template-rows: 10% 90%;

}
</style>
