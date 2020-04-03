<template>
  <div class="content">
    <h1 class="text">She's a designer 🦖</h1>
  </div>
</template>

<script>
export default {
  name: "RightBox"
};
</script>

<style scoped>
.content {
  height: 50vh;
  background-color: green;
  color: white;

  animation-name: rightIn;
  animation-duration: 1s;
  animation-timing-function: ease-in;
}

.text {
  margin: 0;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

@keyframes rightIn {
  0% {
    transform: translateX(100%);
  }
  55% {
    transform: translateX(0%);
  }
  65% {
    transform: translateX(10%);
  }
  75% {
    transform: translateX(0%);
  }
  80% {
    transform: translateX(7%);
  }
  85% {
    transform: translateX(0%);
  }
  90% {
    transform: translateX(5%);
  }
  95% {
    transform: translateX(0%);
  }
  97% {
    transform: translateX(2%);
  }
  100% {
    transform: translateX(0);
  }
}
</style>