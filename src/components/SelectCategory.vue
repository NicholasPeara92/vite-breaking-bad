<script>
import { store } from "../store";
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <section class="container pb-4 pl-3">
    <select
      class="form-select w-auto"
      v-model="store.category"
      aria-label="Default select example"
      @change="$emit('search')"
    >
      <option value="Breaking Bad">Breaking Bad</option>
      <option value="Better Call Saul">Better Call Saul</option>
    </select>
  </section>
</template>

<style lang="scss" scoped></style>
