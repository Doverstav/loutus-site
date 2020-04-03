<template>
  <div class="container">
    <img src="../assets/fireworks.gif" />
    <h1 class="centered">Together they're Loutus 😎</h1>
  </div>
</template>

<script>
export default {
  name: "BigText"
};
</script>

<style scoped>
.container {
  position: relative;
}

.centered {
  color: white;
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>