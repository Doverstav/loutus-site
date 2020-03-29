<template>
  <div class="content">
    <h1 class="text">He's a developer 🤓</h1>
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
}

.text {
  margin: 0;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}

@keyframes leftIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}
</style>