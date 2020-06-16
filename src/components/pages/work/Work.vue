<template>
  <div class="work">
    <div class="work-container">
      <div>
        <h1>Products</h1>
      </div>
      <div class="product-card-grid">
        <Card />
        <Card />
        <Card />
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card";

export default {
  name: "Work",
  components: {
    Card
  }
};
</script>

<style scoped>
.work {
  background-image: linear-gradient(160deg, white 75%, #eaeaea 75%);
}

.work-container {
  box-sizing: border-box;

  height: 100%;
  max-width: 1224px;
  margin: auto;
  padding: 32px;
}

.product-card-grid {
  display: grid;
  justify-items: center;

  grid-template-columns: 1fr 1fr 1fr;
  column-gap: 32px;
}
</style>