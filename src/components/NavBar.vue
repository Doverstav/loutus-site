<template>
  <div class="nav">
    <div class="nav-container">
      <img class="logo-small" src="../assets/loutus_logo_small.svg" />

      <div class="nav-grid-container">
        <span class="nav-link">HOME</span>
        <span class="nav-link">MEET LOUTUS</span>
        <span class="nav-link">WORK</span>
        <span class="nav-link">CONTACT</span>
      </div>
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
  box-shadow: 0 5px 10px #eaeaea;

  /* Ensure that navbar is above content and box-shadow is visible */
  position: relative;
  z-index: 2;
}

.nav-container {
  height: 100%;
  max-width: 1224px;
  margin: auto;

  display: grid;
  grid-template-columns: auto auto;
}

.nav-grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
}

.logo-small {
  height: 50%;
  margin-left: 32px;
  align-self: center;
}

.nav-link {
  align-self: center;
  justify-self: center;

  border-bottom: 4px solid rgba(0, 0, 0, 0);

  font-family: "Maven Pro", sans-serif;
}

.nav-link:hover {
  border-bottom: 4px solid #86c7c4;
  cursor: pointer;
}
</style>