<template>
  <div class="d-flex">
    <div class="col-2 text-center my_card">
      <img src="@/assets/logo.png" alt="" />
      <h3 class="text-white">asdasd</h3>
    </div>
    <div class="col-2 text-center my_card">
      <img src="@/assets/logo.png" alt="" />
      <h3 class="text-white">asdasd</h3>
    </div>
    <div class="col-2 text-center my_card">
      <img src="@/assets/logo.png" alt="" />
      <h3 class="text-white">asdasd</h3>
    </div>
    <div class="col-2 text-center my_card">
      <img src="@/assets/logo.png" alt="" />
      <h3 class="text-white">asdasd</h3>
    </div>
    <div class="col-2 text-center my_card">
      <img src="@/assets/logo.png" alt="" />
      <h3 class="text-white">asdasd</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "SongCard",
  props: {},
};
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables.scss";

.my_card {
  padding: 15px;
  margin: 20px;
  background-color: $primary-color;
  img {
    width: 100%;
  }
}
</style>