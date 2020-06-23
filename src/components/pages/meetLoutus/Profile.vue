<template>
  <div class="profile-container">
    <div class="profile-inner-container">
      <div class="profile-picture-container">
        <img class="profile-picture" :alt="imageAlt" :src="image" />
        <span class="profile-emoji">{{emoji}}</span>
      </div>
      <div class="profile-text-container">
        <div class="profile-text-section">
          <p class="profile-picture-text" :style="textAccent">{{imageText}}</p>
          <p class="profile-bio-text">{{text}}</p>
        </div>
        <div class="profile-email-section">
          <p class="profile-email-header" :style="textAccent">Contact</p>
          <a class="profile-email-address" :href="`mailto:${email}`">{{email}}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    imageAlt: String,
    imageText: String,
    emoji: String,
    text: String,
    email: String,
    accentColor: String
  },
  computed: {
    textAccent () {
      return `color: ${this.accentColor};`;
    }
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

.profile-picture-container {
  position: relative;
}

.profile-picture {
  width: 100%;
}

.profile-emoji {
  font-size: 2em;

  position: absolute;
  right: 8px;
  bottom: -4px;
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

  margin-top: 0;
}

.profile-bio-text {
  font-size: 1em;
}

.profile-email-header {
  font-size: 0.8em;
  text-transform: uppercase;
  margin-bottom: 0;
}

.profile-email-address {
  margin-top: 4px;
  margin-bottom: 0px;

  font-size: 0.8em;
  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}

.profile-email-address:link {
  color: #333333;
}
</style>