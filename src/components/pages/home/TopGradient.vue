<template>
  <div class="top-gradient">
    <div class="top-gradient-container">
      <img alt="Loutus logo" class="loutus-logo" :src="logoPath" />
      <p
        class="top-gradient-text"
      >We are a dream team delivering stunning UI, UX and web design, responsively and professionally implemented.</p>
      <a class="top-gradient-link" href="/" @click="navigateToMeet">Get to know us ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopGradient",
  computed: {
    logoPath() {
      // Add current time to path to logo. This should stop
      // caching of the SVG-file and ensure that the animation
      // plays every time the site is reloaded
      return `${require("../../../assets/loutus_logo.svg")}?${Date.now()}`;
    }
  },
  methods: {
    navigateToMeet(event) {
      event.preventDefault();
      window.history.pushState(null, "", "/meet-loutus");
      // Make sure that things update
      dispatchEvent(new PopStateEvent("popstate"));
    }
  }
};
</script>

<style scoped>
.top-gradient {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-image: linear-gradient(170deg, white 50%, rgba(0, 0, 0, 0) 50%);

  z-index: 1;
}

.top-gradient-container {
  box-sizing: border-box;

  height: 100%;
  max-width: 1224px;

  margin: auto;
  padding-left: 32px;
  padding-right: 32px;
  padding-bottom: 32px;

  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.loutus-logo {
  margin-top: 128px;

  max-width: 100%;
}

.top-gradient-text {
  margin-top: 32px;
  max-width: 350px;
  text-align: start;

  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}

.top-gradient-link {
  color: #86c7c4;
  text-transform: uppercase;

  font-family: "Maven Pro", sans-serif;
}

@media screen and (max-width: 540px) {
  .loutus-logo {
    margin-top: 64px;
  }
}
</style>