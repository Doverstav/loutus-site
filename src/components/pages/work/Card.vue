<template>
  <div class="card">
    <div class="card-header">
      <img class="card-image" :src="imagePath" />
    </div>
    <div class="card-body">
      <h2 class="text card-header">{{header}}</h2>
      <p class="text card-text">{{text}}</p>
      <a class="text card-link" :href="linkHref">{{linkText}}</a>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      random: Math.floor(Math.random()*100)
    }
  },
  props: {
    imagePath: String,
    header: String,
    text: String,
    linkText: String,
    linkHref: String
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