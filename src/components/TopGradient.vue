<template>
  <div class="top-gradient">
    <div class="top-gradient-container">
      <img class="loutus-logo" src="../assets/loutus_logo.svg" />
      <p
        class="top-gradient-text"
      >We create digital products that are totally awesome. We create digital products that are totally awesome. We create digital products that are totally awesome.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopGradient",
  data: function() {
    return {
      logoPath: "../assets/loutus_logo.svg"
    };
  },
  mounted: function() {
    // Add current time to path to logo. This should stop 
    // caching of the SVG-file and ensure that the animation
    // plays every time the site is reloaded
    let logo = document.querySelector(".loutus-logo");
    logo.src = `${logo.src}?${Date.now()}`;
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
  height: 100%;
  max-width: 1224px;
  margin: auto;
  position: relative;
}

.loutus-logo {
  position: absolute;
  left: 32px;
  top: 25%;
  float: left;

  max-width: 100%;
}

.top-gradient-text {
  position: absolute;
  bottom: 10%;
  left: 2em;

  max-width: 350px;
  text-align: start;

  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}
</style>