<template>
  <div class="nav">
    <div class="nav-container">
      <img class="logo-small" @click="goHome()" src="../../assets/loutus_logo_small.svg" />

      <div class="nav-grid-container">
        <NavLink text="HOME" href="/" />
        <NavLink text="MEET LOUTUS" href="/meet-loutus" />
        <NavLink text="WORK" href="/work" />
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
  },
  methods: {
    goHome() {
      // Only push new state if we are trying to leave current state
      if (window.location.pathname !== "/") {
        window.history.pushState(null, "", "/");
        // Make sure that things update
        dispatchEvent(new PopStateEvent("popstate"));
      }
    }
  }
};
</script>

<style scoped>
.nav {
  width: 100%;
  background-color: white;
  box-shadow: 0 5px 10px #eaeaea;

  /* Ensure that navbar is above content and box-shadow is visible */
  position: relative;
  z-index: 100;
}

.nav-container {
  box-sizing: border-box;
  height: 100%;

  max-width: 1224px;
  margin: auto;
  padding-left: 32px;
  padding-right: 32px;

  display: grid;
  grid-template-columns: auto auto;
}

.nav-grid-container {
  display: grid;
  grid-template-columns: auto auto auto;
}

.logo-small {
  height: 50%;
  align-self: center;
}

.logo-small:hover {
  cursor: pointer;
}
</style>