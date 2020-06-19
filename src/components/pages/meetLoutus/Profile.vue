<template>
  <div class="profile-container">
    <div class="profile-inner-container">
      <div class="profile-picture-container">
        <img class="profile-picture" :src="image" />
        <p class="profile-emoji">{{emoji}}</p>
      </div>
      <div class="profile-text-container">
        <p class="profile-picture-text">{{imageText}}</p>
        <p class="profile-bio-text">{{text}}</p>
        <p>Contact</p>
        <p>{{email}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    imageText: String,
    emoji: String,
    text: String,
    email: String
  }
};
</script>

<style scoped>
.profile-container {
  width: 100%;
  background-color: white;
  border-radius: 5px;
  box-shadow: 0 16px 24px rgba(0, 29, 63, 0.14);

  overflow: hidden; /* Ensure that images get rounded corners */
}

.profile-picture {
  width: 100%;
}

.profile-text-container {
  text-align: start;
  margin: 16px;
}

.profile-picture-text {
  font-size: 1.2em;
  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}

.profile-bio-text {
  font-family: "Maven Pro", sans-serif;
}
</style>