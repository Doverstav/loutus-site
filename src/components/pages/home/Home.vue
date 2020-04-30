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
  /* Needed because child elements use absolute positioning. */
  position: relative; 
}
</style>