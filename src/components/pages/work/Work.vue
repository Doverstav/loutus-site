<template>
  <div>
    <div class="background-container"></div>
    <div class="work">
      <div class="work-container">
        <div class="work-header-container">
          <h1 class="work-heading-large">Products</h1>
          <h2 class="work-heading-small">We've created</h2>
        </div>
        <div class="product-card-grid">
          <Card
            v-for="card in cards"
            :key="card.text"
            :imagePath="card.imagePath"
            :header="card.header"
            :text="card.text"
            :linkText="card.linkText"
            :linkHref="card.linkHref"
          />
        </div>
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
  },
  data() {
    return {
      cards: [
        {
          imagePath: `https://picsum.photos/500/300?random=random${Math.floor(
            Math.random() * 100
          )}`,
          header: "Website",
          text:
            "Cat ipsum dolor sit amet, furrier and even more furrier hairball but please stop looking at your phone and pet me find empty spot in cupboard and sleep all day yet kitty.",
          linkText: "More plz >",
          linkHref: "google.com"
        },
        {
          imagePath: `https://picsum.photos/500/300?random=random${Math.floor(
            Math.random() * 100
          )}`,
          header: "Website",
          text:
            "Cat ipsum dolor sit amet, furrier and even more furrier hairball but please stop looking at your phone and pet me find empty spot in cupboard and sleep all day yet kitty.",
          linkText: "More plz >",
          linkHref: "google.com"
        },
        {
          imagePath: `https://picsum.photos/500/300?random=random${Math.floor(
            Math.random() * 100
          )}`,
          header: "Website",
          text:
            "Cat ipsum dolor sit amet, furrier and even more furrier hairball but please stop looking at your phone and pet me find empty spot in cupboard and sleep all day yet kitty.",
          linkText: "More plz >",
          linkHref: "google.com"
        },
        {
          imagePath: `https://picsum.photos/500/300?random=random${Math.floor(
            Math.random() * 100
          )}`,
          header: "Website",
          text:
            "Cat ipsum dolor sit amet, furrier and even more furrier hairball but please stop looking at your phone and pet me find empty spot in cupboard and sleep all day yet kitty.",
          linkText: "More plz >",
          linkHref: "google.com"
        },
        {
          imagePath: `https://picsum.photos/500/300?random=random${Math.floor(
            Math.random() * 100
          )}`,
          header: "Website",
          text:
            "Cat ipsum dolor sit amet, furrier and even more furrier hairball but please stop looking at your phone and pet me find empty spot in cupboard and sleep all day yet kitty.",
          linkText: "More plz >",
          linkHref: "google.com"
        }
      ]
    };
  }
};
</script>

<style scoped>
.background-container {
  z-index: 9;

  position: absolute;
  left: 0;
  top: 0;
  height: 100vh;
  width: 100%;
  background-image: linear-gradient(172deg, white 65%, #eaeaea 65%);
}

.work {
  position: relative;
  z-index: 10;
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