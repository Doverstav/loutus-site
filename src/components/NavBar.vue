<template>
  <div class="nav"></div>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style scoped>
.nav {
  height: 10vh;
  width: 100%;
  background-color: white;
  box-shadow: 0 5px 10px lightgray;
  position: relative; /* Ensure that navbar is above content and box-shadow is visible */
  z-index: 2;
}
</style>