<template>
  <div class="input-group mb-3" style="color: white">
    <select
      class="custom-select"
      name=""
      id=""
      @change="$emit(`onchange`, value)"
      v-model="value"
    >
      <option selected>Scegli un genere...</option>
      <option>rock</option>
      <option>metal</option>
      <option>jazz</option>
      <option>rock</option>
      <option>rock</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "SelectGenre",
  props: ["arraygeneri", "genere"],
  data() {
    return {
      value: "",
    };
  },
  computed: {},
};
</script>

<style scoped lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "@/styles/variables";
</style>