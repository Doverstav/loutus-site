<template>
  <div class="top-gradient">
    <img class="top-gradient-text" src="../assets/loutus_logo.svg" />
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

  animation-name: leftIn;
  animation-duration: 1s;

  z-index: 1;
}

.top-gradient-text {
  position: absolute;
  top: 25%;
  left: 2em;

  /*opacity: 0;

  animation-delay: 1s;
  animation-name: fadeIn;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;*/
}

@keyframes leftIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>