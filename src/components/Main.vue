<template>
  <div>
    <div class="main">
      <div class="container">
        <div class="row">
          <SongCard />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SongCard from "./SongCard.vue";
export default {
  components: { SongCard },
  name: "Main",
  props: {},
};
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables.scss";

.main {
  background-color: $secondary-color;
  height: calc(100vh - 60px);
}
</style>
