<template>
  <div class="content">
    <h1 class="text">He's a developer 🤖</h1>
  </div>
</template>

<script>
export default {
  name: "LeftBox"
};
</script>

<style scoped>
.content {
  height: 50vh;
  background-color: blue;
  color: white;

  animation-name: leftIn;
  animation-duration: 1s;
  animation-timing-function: ease-in;
}

.text {
  margin: 0;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

@keyframes leftIn {
  0% {
    transform: translateX(-100%);
  }
  55% {
    transform: translateX(0%);
  }
  65% {
    transform: translateX(-10%);
  }
  75% {
    transform: translateX(0%);
  }
  80% {
    transform: translateX(-7%);
  }
  85% {
    transform: translateX(0%);
  }
  90% {
    transform: translateX(-5%);
  }
  95% {
    transform: translateX(0%);
  }
  97% {
    transform: translateX(-2%);
  }
  100% {
    transform: translateX(0);
  }
}
</style>