<template>
  <div class="meet-loutus">
    <div class="meet-loutus-container">
      <div class="meet-loutus-box profile-texts">
        <div class="profile-text-container">
          <h1 class="profile-text profile-text-first">Hi there</h1>
          <h1 class="profile-text profile-text-second">We're</h1>
          <img class="profile-text-logo" src="../../../assets/loutus_logo_no_text.svg" />
          <p class="profile-text-description">We create design and blip-blop. This is what we do. If you ask us what we do - that would be our answer.</p>
        </div>
      </div>
      <div class="meet-loutus-box profiles">
        <Profile
          :image="louData.profile"
          :imageText="louData.profileText"
          :emoji="louData.emoji"
          :text="louData.text"
        />
        <Profile
          :image="tusData.profile"
          :imageText="tusData.profileText"
          :emoji="tusData.emoji"
          :text="tusData.text"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Profile from "./Profile";

export default {
  name: "MeetLoutus",
  data() {
    return {
      louData: {
        profile: require(`../../../assets/profile_lou.png`),
        profileText: "She's a designer.",
        emoji: "🦖",
        text:
          "This is Louise. She is a dinosaur. But she pretends to be a designer so that people will hire her. People think that dinosaurs can’t do design. And that is true because they are extinct."
      },
      tusData: {
        profile: require(`../../../assets/profile_tus.png`),
        profileText: "He's a developer.",
        emoji: "🤖",
        text:
          "This is Pontus. He does the blip-blop like a robot, so you can understand why his emoticon is a robot. His habitat is inside the [blip-blop] box. He likes it there."
      }
    };
  },
  components: {
    Profile
  }
};
</script>

<style scoped>
.meet-loutus {
  background-image: linear-gradient(160deg, white 75%, #eaeaea 75%);
}

.meet-loutus-container {
  box-sizing: border-box;
  
  height: 100%;
  max-width: 1224px;

  margin: auto;
  padding-right: 32px;
  padding-left: 32px;

  display: grid;
  grid-template-columns: 1fr 1fr;
}

.profiles {
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 16px;

  margin-top: 50%;

  height: fit-content;
}

.profile-text-container {
  margin-top: 50%;
  text-align: left;
}

.profile-text {
  font-family: "Maven Pro", sans-serif;
  font-weight: 600;
  text-transform: uppercase;
  margin-top: 4px;
  margin-bottom: 4px;
}

.profile-text-first {
  position: relative;
  left: 7%;

  font-size: 25px;
}

.profile-text-second {
  position: relative;
  left: 15%;

  font-size: 45px;
  color: #86c7c4;
}

.profile-text-logo {
  max-width: calc(100% - 32px);
}

.profile-text-description {
  max-width: 50%;
  margin-top: 64px;

  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}
</style>