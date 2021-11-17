<template>
  <div>
    <div class="main">
      <div class="my_container">
        <SelectGenre
          :genere="genre"
          :arraygeneri="brani"
          @onchange="takeValue"
        ></SelectGenre>
        <div class="row justify-content-center">
          <SongCard
            v-for="(song, i) in showFilteredData"
            :key="i"
            :img="song.poster"
            :autore="song.author"
            :titolo="song.title"
            :anno="song.year"
            :genere="song.genre"
          ></SongCard>
          <!-- {{ genreFilter() }} -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SongCard from "./SongCard.vue";
import axios from "axios";
import "@fontsource/montserrat";
import SelectGenre from "./SelectGenre.vue";

export default {
  components: { SongCard, SelectGenre },
  name: "Main",
  data() {
    return {
      brani: [],
      selectedOption: "",
    };
  },
  methods: {
    onClickFilter() {
      return console.log(this.value);
    },
    arraygeneri() {
      let arraygenre = [];
      this.brani.forEach((element) => {
        let generi = element.genre;

        if (arraygenre.includes(generi) === undefined) {
          arraygenre.push(generi);
        }
      });
      console.log(arraygenre);
      return arraygenre;
    },
    takeValue(value) {
      this.selectedOption = value;
    },
  },
  computed: {},
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((songObj) => {
        this.brani = songObj.data.response;
      });
  },
  showFilteredData() {
    if (this.brani.genre.includes(this.selectedOption)) {
      return;
    }
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
