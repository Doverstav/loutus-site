<template>
  <div class="bottom-gradient">
    <img class="cool-keyboard" src="../assets/keyboard.png" />
  </div>
</template>

<script>
export default {
  name: "BottomGradient"
}
</script>

<style scoped>
.bottom-gradient {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-image: linear-gradient(170deg, rgba(0,0,0,0) 50%, lightgrey 50%);

  /*animation-name: rightIn;
  animation-duration: 1s;*/
}

.cool-keyboard {
  position: absolute;
  bottom: 5em;
  right: 5em;

  /*opacity: 0;

  animation-delay: 1s;
  animation-name: fadeIn;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;*/
}

@keyframes rightIn {
  from {
    transform: translateX(100%);
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