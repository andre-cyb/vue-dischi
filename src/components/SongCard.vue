<template>
  <div class="col-2 text-center my_card">
    <img :src="img" alt="" />
    <h4 class="text-white m-0 pt-4 pb-4">{{ titolo }}</h4>
    <span>{{ autore }}</span>
    <small>{{ anno }}</small>
  </div>
</template>




<script>
export default {
  name: "SongCard",
  props: ["autore", "genere", "img", "titolo", "anno"],
};
</script>




<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables.scss";

.my_card {
  color: white;
  padding: 15px;
  margin: 20px;
  background-color: $primary-color;
  img {
    width: 100%;
  }
  h4 {
    text-transform: uppercase;
    font-weight: 800;
    font-size: 22px;
  }
  span {
    display: block;
    color: $secondary-text-color;
    font-weight: 700;
  }
  small {
    color: $secondary-text-color;
    font-weight: 700;
  }
}
</style>