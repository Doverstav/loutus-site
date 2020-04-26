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
  name: "Home",
  components: {
    TopGradient,
    BottomGradient
  }
}
</script>

<style scoped>
.double-gradient {
  height: 90vh;
  position: relative;
}
</style>