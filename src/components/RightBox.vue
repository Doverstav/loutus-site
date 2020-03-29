<template>
  <div class="content">
    <h1 class="text">She's a designer 🤩</h1>
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
}

.text {
  margin: 0;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

@keyframes rightIn {
  from {
    transform: translate3d(100%, 0, 0);
  }
  to {
    transform: translate3d(0, 0, 0);
  }
}
</style>