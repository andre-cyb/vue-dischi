<template>
  <div>
    <div class="main">
      <div class="my_container">
        <div class="row justify-content-center">
          <SongCard
            v-for="(song, i) in brani"
            :key="i"
            :img="song.poster"
            :autore="song.author"
            :titolo="song.title"
            :anno="song.year"
            :genere="song.genre"
          ></SongCard>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SongCard from "./SongCard.vue";
import axios from "axios";
import "@fontsource/montserrat";
export default {
  components: { SongCard },
  name: "Main",
  data() {
    return {
      brani: [],
    };
  },
  methods: {},
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((songObj) => {
        this.brani = songObj.data.response;
      });
  },
};
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables.scss";

.main {
  display: flex;
  background-color: $secondary-color;
  height: calc(100vh - 66px);
  .my_container {
    max-width: 1180px;
    margin: auto;
  }
}
</style>
