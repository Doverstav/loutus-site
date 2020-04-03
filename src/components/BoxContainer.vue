<template>
  <div class="container">
    <LeftBox />
    <RightBox />
  </div>
</template>

<script>
import LeftBox from "./LeftBox";
import RightBox from "./RightBox";

export default {
  name: "BoxContainer",
  components: {
    LeftBox,
    RightBox
  }
};
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: auto auto;
}
</style>