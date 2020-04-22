<template>
  <div class="nav">

    <img class="logo-small" src="../assets/logo_small.png" />

    <div class="nav-grid-container">
      <span class="nav-link">HOME</span>
      <span class="nav-link">MEET LOUTUS</span>
      <span class="nav-link">WORK</span>
      <span class="nav-link">CONTACT</span>
    </div>
  </div>
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

  display: grid;
  grid-template-columns: auto auto;

  /* Ensure that navbar is above content and box-shadow is visible */
  position: relative;
  z-index: 2;
}

.nav-grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
}

.logo-small {
  height: 75%;
  margin: 8px;
}

.nav-link {
  font-family: 'Maven Pro', sans-serif;
  align-self: center;
}
</style>