<template>
  <div class="meet-loutus">
    <div class="meet-loutus-container">
      <div class="meet-loutus-box profile-texts">
        <div class="profile-text-container">
          <h1 class="profile-text profile-text-first">Hi there</h1>
          <h1 class="profile-text profile-text-second">Nice to meet you</h1>
          <p class="profile-text-description">We are a dream team delivering stunning UI, UX and web design, responsively and professionally implemented.</p>
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
</template>

<script>
import Profile from "./Profile";

export default {
  name: "MeetLoutus",
  data() {
    return {
      profiles: require("../../../assets/data/profiles")
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