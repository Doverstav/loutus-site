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
  padding-right: 32px;
  padding-left: 32px;
  padding-bottom: 32px;
}

.work-header-container {
  margin-top: 128px;
  margin-bottom: 64px;

  text-align: start;

  font-family: "Maven Pro", sans-serif;
  text-transform: uppercase;
}

.work-heading-large {
  font-size: 60px;
  font-weight: 600;
  color: #86c7c4;

  margin: 0;
}

.work-heading-small {
  font-size: 25px;
  font-weight: 600;
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

/* On medium screen, display two products per row */
@media screen and (max-width: 960px) {
  .product-card-grid {
    grid-template-columns: 1fr 1fr;
  }
}

/* On small screen, display one products per row */
@media screen and (max-width: 540px) {
  .product-card-grid {
    grid-template-columns: 1fr;
  }

  .work-header-container {
    margin-top: 64px;
  }
}
</style>