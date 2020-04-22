<template>
  <div class="double-gradient">
    <TopGradient />
    <BottomGradient />
  </div>
</template>

<script>
import TopGradient from "./TopGradient";
import BottomGradient from "./BottomGradient"

export default {
  name: "DoubleGradient",
  components: {
    TopGradient,
    BottomGradient
  }
}
</script>

<style scoped>
.double-gradient {
  height: 50vh;
  position: relative;
}
</style>