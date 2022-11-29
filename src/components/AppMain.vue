<script>
import axios from "axios";
import { store } from "../store";
import SelectCategory from "./SelectCategory.vue";
import CharactersSection from "./CharactersSection.vue";

export default {
  components: {
    SelectCategory,
    CharactersSection,
  },
  data() {
    return {
      store,
    };
  },
  methods: {
    filterCategory() {
      axios
        .get("https://www.breakingbadapi.com/api/characters", {
          params: {
            category: this.store.category,
          },
        })
        .then((resp) => {
          this.store.characters = resp.data;
          console.log(resp);
        });
    },
  },
  created() {
    this.filterCategory();
  },
};
</script>

<template>
  <SelectCategory @search="filterCategory" />
  <CharactersSection />
</template>

<style lang="scss" scoped></style>
