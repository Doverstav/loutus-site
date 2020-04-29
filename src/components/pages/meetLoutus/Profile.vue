<template>
  <div>
    <img :src="image"/>
    {{imageText}}
    {{emoji}}
    {{text}}
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    imageText: String,
    emoji: String,
    text: String,
  }
}
</script>