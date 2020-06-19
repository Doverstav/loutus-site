<template>
  <div class="profile-container">
    <div class="profile-inner-container">
      <div class="profile-picture-container">
        <img class="profile-picture" :src="image" />
        <p class="profile-emoji">{{emoji}}</p>
      </div>
      <div class="profile-text-container">
        <div class="profile-text-section">
          <p class="profile-picture-text">{{imageText}}</p>
          <p class="profile-bio-text">{{text}}</p>
        </div>
        <div class="profile-email-section">
          <p class="profile-email-header">Contact</p>
          <p class="profile-email-address">{{email}}</p>
        </div>
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

.profile-inner-container {
  height: 100%;

  display: grid;
  grid-template-rows: auto 1fr;
}

.profile-picture {
  width: 100%;
}

.profile-text-container {
  font-family: "Maven Pro", sans-serif;

  text-align: start;
  margin: 16px;

  display: grid;
  grid-template-rows: 1fr auto;
}

.profile-picture-text {
  font-size: 1.2em;
  font-weight: 600;
  text-transform: uppercase;
}

.profile-bio-text {
  font-size: 1em;
}

.profile-email-header {
  font-size: 0.8em;
  text-transform: uppercase;
}

.profile-email-address {
  font-size: 0.8em;
  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}
</style>