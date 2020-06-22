<template>
  <div>
    <div class="background-container"></div>
    <div class="meet-loutus">
      <div class="meet-loutus-container">
        <div class="meet-loutus-box profile-texts">
          <div class="profile-text-container">
            <h1 class="profile-text profile-text-first">Hi there</h1>
            <h1 class="profile-text profile-text-second">Nice to meet you</h1>
            <p
              class="profile-text-description"
            >We are a dream team delivering stunning UI, UX and web design, responsively and professionally implemented.</p>
          </div>
        </div>
        <div class="meet-loutus-box profiles">
          <Profile
            v-for="profile in profiles"
            :key="profile.emoji"
            :image="profile.profile"
            :imageText="profile.profileText"
            :emoji="profile.emoji"
            :text="profile.text"
            :email="profile.email"
            :accentColor="profile.accentColor"
          />
        </div>
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
      profiles: [
        {
          profile: require("@/assets/profile_lou.png"),
          profileText: "She's a designer.",
          emoji: "🦖",
          text:
            "This is Louise. She is a dinosaur. But she pretends to be a designer so that people will hire her. People think that dinosaurs can’t do design. And that is true because they are extinct.",
          email: "lou@loutus.com",
          accentColor: "#97CC2B"
        },
        {
          profile: require("@/assets/profile_tus.png"),
          profileText: "He's a developer.",
          emoji: "🤖",
          text:
            "This is Pontus. He does the blip-blop like a robot, so you can understand why his emoticon is a robot. His habitat is inside the [blip-blop] box. He likes it there.",
          email: "tus@loutus.com",
          accentColor: "#86c7c4"
        }
      ]
    };
  },
  components: {
    Profile
  }
};
</script>

<style scoped>
.meet-loutus {
  position: relative;
  z-index: 10;
}

.background-container {
  z-index: 9;

  position: absolute;
  left: 0;
  top: 0;
  height: 100vh;
  width: 100%;
  background-image: linear-gradient(170deg, white 65%, #eaeaea 65%);
}

.meet-loutus-container {
  box-sizing: border-box;

  height: 100%;
  max-width: 1224px;

  margin: auto;
  padding-right: 32px;
  padding-left: 32px;
  padding-bottom: 32px;

  display: grid;
  grid-template-columns: 1fr 1fr;
}

/* 
  For medium screens, display profiles content in two rows
  Introductory text in top row, and profiles side by side in second row
 */
@media screen and (max-width: 960px) {
  .meet-loutus-container {
    grid-template-columns: 1fr;
  }
}

.profiles {
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 32px;
  row-gap: 32px;

  margin-top: 128px;

  height: fit-content;
}

/*
  For small screens, display in three rows. Text first, then profiles
  in separate rows.
*/
@media screen and (max-width: 540px) {
  .profiles {
    grid-template-columns: 1fr;
  }
}

.profile-text-container {
  margin-top: 128px;
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
  font-size: 50px;
  color: #86c7c4;
}

.profile-text-second {
  margin-left: 20%;

  font-size: 25px;
}

.profile-text-description {
  max-width: 65%;
  margin-top: 32px;

  font-family: Courier New, Courier, Lucida Sans Typewriter, Lucida Typewriter,
    monospace;
}

@media screen and (max-width: 540px) {
  .profile-text-description {
    max-width: 100%;
  }

  .profiles {
    margin-top: 64px;
  }

  .profile-text-container {
    margin-top: 64px;
  }
}
</style>