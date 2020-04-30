<template>
  <div class="profile-container">
    <div class="profile-inner-container">
      <div class="profile-picture-container">
        <img class="profile-picture" :src="image" />
        <p class="profile-emoji">{{emoji}}</p>
      </div>
      <p class="profile-picture-text">{{imageText}}</p>
      <p class="profile-bio-text">{{text}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    imageText: String,
    emoji: String,
    text: String
  }
};
</script>

<style scoped>
.profile-container {
  position: relative;
  text-align: left;

  margin-left: 32px;
  margin-right: 32px;
}

.profile-inner-container {
  position: absolute;
  left: 0;
  top: 35%;
}

.profile-picture-container {
  position: relative;
}

.profile-emoji {
  position: absolute;
  bottom: 0;
  left: 0;

  font-size: 3em;
  margin: 0;
}

.profile-picture {
  width: 75%;
  display: block;
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