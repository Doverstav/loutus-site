<template>
  <div class="card">
    <div class="card-header">
      <img class="card-image" :src="`https://picsum.photos/500/300?random=random${random}`" />
    </div>
    <div class="card-body">
      <h2 class="text card-header">WEBSITE</h2>
      <p class="text card-text">Cat ipsum dolor sit amet, furrier and even more furrier hairball but please stop looking at your phone and pet me find empty spot in cupboard and sleep all day yet kitty.</p>
      <a class="text card-link" href="google.com">MORE PLZ ></a>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      random: Math.floor(Math.random()*100)
    }
  }
}
</script>

<style scoped>
.card:nth-child(odd) .card-header {
  color: #86c7c4;
}

.card:nth-child(odd) .card-link:link {
  color: #86c7c4;
}

.card:nth-child(even) .card-link:link {
  color: black;
}

.card {
  width: 100%;
  background-color: white;
  border-radius: 5px;
  box-shadow: 0 16px 24px rgba(0, 29, 63, 0.14);

  overflow: hidden; /* Ensure that images get rounded corners */
}

.card-image {
  width: 100%;
}

.card-body {
  text-align: start;
  margin: 16px;
}

.text {
  font-family: "Maven Pro", sans-serif;
}

.card-header {
  font-size: 20px;
}

.card-text {
  font-size: 12px;
}

.card-link {
  font-size: 12px;
}
</style>