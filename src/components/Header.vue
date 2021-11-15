<template>
  <div>
    <div class="header">
      <img class="ps-2" src="@/assets/logo-small.svg" width="50px" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {},
};
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables";

.header {
  background-color: $primary-color;
  padding: 12px;
}
</style>
