<template>
  <div class="work">
    <div class="work-container">
      <div class="work-header-container">
        <h1 class="work-heading-large">Products</h1>
        <h2 class="work-heading-small">We've created</h2>
      </div>
      <div class="product-card-grid">
        <Card />
        <Card />
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

.work-header-container {
  margin-top: 12%;
  margin-bottom: 6%;

  text-align: start;

  font-family: "Maven Pro", sans-serif;
  font-weight: 600;
  text-transform: uppercase;
}

.work-heading-large {
  font-size: 45px;
  color: #86c7c4;

  margin: 0;
}

.work-heading-small {
  font-size: 25px;
  color: #333333;

  margin: 0;
  margin-left: 100px;
}

.product-card-grid {
  display: grid;
  justify-items: center;

  grid-template-columns: 1fr 1fr 1fr;
  column-gap: 32px;
  row-gap: 32px;
}
</style>