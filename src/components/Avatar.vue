<template>
<figure class="avatar">
  <img :src="src"
       :alt="alt"
       :width="size"
       :height="size"
  >
</figure>
</template>

<script>
export default {
  name: "Avatar",
  props : {
    src: {
      type: String,
      default : 'https://media.discordapp.net/attachments/986699863938990082/989978347603918898/frog.png'
    },
    alt : {
      type: String
    },
    size : {
      type: Number
    }
  }
};
</script>

<style scoped>

.avatar {
  padding:  2px;
  border-radius: 999px;
  display: inline-flex;
  background: linear-gradient(
      219deg,
      rgba(184, 63, 140, 1) 0%,
      rgba(237, 158, 90, 1) 100%
  );
  img{
    border-radius: inherit;
    border:2px solid white
  }
}
</style>