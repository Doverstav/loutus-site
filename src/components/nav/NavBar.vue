<template>
  <div class="nav">
    <div class="nav-container">
      <img class="logo-small" @click="goHome()" src="../../assets/loutus_logo_small.svg" />

      <div class="nav-grid-container">
        <NavLink text="HOME" href="/" />
        <NavLink text="MEET LOUTUS" href="/meet-loutus" />
        <NavLink text="WORK" href="/work" />
      </div>
      <div class="mobile-nav-container">
        <img src="../../assets/icons/menu.svg" @click="togglePanel()">
        <div class="mobile-nav-panel" :class="{'display-panel': showPanel}">
          <div>
            <img class="close-nav-button" src="../../assets/icons/x.svg" @click="togglePanel()">
          </div>
          <div class="mobile-nav-grid">
            <NavLink text="HOME" href="/" />
            <NavLink text="MEET LOUTUS" href="/meet-loutus" />
            <NavLink text="WORK" href="/work" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavLink from "./NavLink";

export default {
  name: "NavBar",
  data: function() {
    return {
      showPanel: false
    };
  },
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
    },
    togglePanel() {
      this.showPanel = !this.showPanel;
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
  align-items: center;
}

.nav-grid-container {
  display: grid;
  grid-template-columns: auto auto auto;
}

.mobile-nav-container {
  justify-self: end;
  display: none;
}

.mobile-nav-grid {
  box-sizing: border-box;
  padding: 32px;

  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-content: flex-start;
}

.mobile-nav-grid > * {
  font-size: 25px;
  margin-top: 16px;
  margin-bottom: 16px;
}

.mobile-nav-panel {
  position: fixed;
  right: 0;
  top: 0;

  height: 100vh;
  width: 90vw;

  transform: translateX(100%);

  overflow-x: hidden;
  transition: 0.5s; /* .5s animation when changing width */

  background-color: white;
}

.close-nav-button {
  position: absolute;
  top: 32px;
  right: 32px;
}

.display-panel {
  transform: translateX(0);
  box-shadow: 2px 4px 50px rgba(0, 0, 0, 0.15);
}

.logo-small {
  height: 50%;
}

.logo-small:hover {
  cursor: pointer;
}

/* Decide which nav to display based on screen size */
@media screen and (max-width: 540px) {
  .nav-grid-container {
    display: none;
  }

  .mobile-nav-container {
    display: block;
  }
}

</style>