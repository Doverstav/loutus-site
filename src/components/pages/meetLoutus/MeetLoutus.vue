<template>
  <div class="meet-loutus">
    <div class="meet-loutus-container">
      <div class="meet-loutus-box">
        <p>Here is some text!</p>
      </div>
      <div class="meet-loutus-box">
        <Profile :image="louData.profile" :imageText="louData.profileText" :emoji="louData.emoji" :text="louData.text" />
        <Profile :image="tusData.profile" :imageText="tusData.profileText" :emoji="tusData.emoji" :text="tusData.text" />
      </div>
    </div>
  </div>
</template>

<script>
import Profile from "./Profile";

export default {
  name: "MeetLoutus",
  components: {
    Profile
  },
  computed: {
    louData: function() {
      return {
        profile: require(`../../../assets/profile_lou.png`),
        profileText: "She's a designer",
        emoji: "🦖",
        text:
          "This is Louise. She is a dinosaur. But she pretends to be a designer so that people will hire her. People think that dinosaurs can’t do design. And that is true because they are extinct."
      };
    },
    tusData: function() {
      return {
        profile: require(`../../../assets/profile_tus.png`),
        profileText: "He's a developer",
        emoji: "🤖",
        text:
          "This is Pontus. He does the blip-blop like a robot, so you can understand why his emoticon is a robot. His habitat is inside the [blip-blop] box. He likes it there."
      };
    }
  }
};
</script>

<style scoped>
.meet-loutus {
  background-image: linear-gradient(160deg, white 75%, #eaeaea 75%);
}

.meet-loutus-container {
  height: 100%;
  max-width: 1224px;
  margin: auto;

  display: grid;
  grid-template-columns: 50% 50%;
}

.meet-loutus-box {
  height: 100%;
}
</style>