<template>
  <div class="top-gradient">
    <img class="loutus-logo" src="../assets/loutus_logo.svg" />
  </div>
</template>

<script>
export default {
  name: "TopGradient"
}
</script>

<style scoped>
.top-gradient {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-image: linear-gradient(170deg, white 50%, rgba(0,0,0,0) 50%);

  z-index: 1;
}

.loutus-logo {
  position: absolute;
  top: 25%;
  left: 2em;

  max-width: 100%;
}
</style>