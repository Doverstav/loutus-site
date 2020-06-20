<template>
  <div class="nav">
    <div class="nav-container">
      <img class="logo-small" @click="goHome()" src="../../assets/loutus_logo_small.svg" />

      <div v-if="!isMobile" class="nav-grid-container">
        <NavLink text="HOME" href="/" />
        <NavLink text="MEET LOUTUS" href="/meet-loutus" />
        <NavLink text="WORK" href="/work" />
      </div>
      <div v-else class="mobile-nav-container">
        <span @click="togglePanel()">@</span>
        <div class="mobile-nav-panel" :class="{'display-panel': showPanel}">
          <div>
            <span @click="togglePanel()">@</span>
          </div>
          <div>
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
  computed: {
    isMobile() {
      return window.matchMedia("(max-width: 540px").matches;
    }
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
}

.nav-grid-container {
  display: grid;
  grid-template-columns: auto auto auto;
}

.mobile-nav-panel {
  position: fixed;
  right: 0;
  top: 0;

  height: 100vh;
  width: 0;

  overflow-x: hidden;
  transition: 0.5s; /* .5s animation when changing width */

  background-color: white;
  box-shadow: 2px 4px 50px rgba(0, 0, 0, 0.15);
}

.display-panel {
  width: 90vw;
}

.logo-small {
  height: 50%;
  align-self: center;
}

.logo-small:hover {
  cursor: pointer;
}
</style>