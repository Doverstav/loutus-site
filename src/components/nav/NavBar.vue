<template>
  <div class="nav">
    <div class="nav-container">
      <img class="logo-small" src="../../assets/loutus_logo_small.svg" />

      <div class="nav-grid-container">
        <NavLink text="HOME" href="/" />
        <NavLink text="MEET LOUTUS" href="/meet-loutus" />
        <NavLink text="WORK" href="/work" />
        <NavLink text="CONTACT" href="/contact" />
      </div>
    </div>
  </div>
</template>

<script>
import NavLink from "./NavLink";

export default {
  name: "NavBar",
  components: {
    NavLink
  }
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
</style>