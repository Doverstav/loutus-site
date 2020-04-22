<template>
  <div class="bottom-gradient">
    <img class="cool-keyboard" src="../assets/keyboard.png" />
  </div>
</template>

<script>
export default {
  name: "BottomGradient"
};
</script>

<style scoped>
.bottom-gradient {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-image: linear-gradient(170deg, rgba(0, 0, 0, 0) 50%, #eaeaea 50%);
}

.cool-keyboard {
  position: absolute;
  bottom: 0;
  right: 0;

  height: 100%;
}
</style>