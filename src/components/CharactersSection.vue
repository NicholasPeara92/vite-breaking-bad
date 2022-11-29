<script>
import { store } from "../store";
import CharacterCard from "./CharacterCard.vue";

export default {
  components: {
    CharacterCard,
  },
  data() {
    return {
      store,
    };
  },
  computed: {
    totalCharacters() {
      return store.characters.length;
    },
  },
};
</script>

<template>
  <section class="container p-5">
    <div id="chars-founded" class="p-3">
      <h3>Found {{ totalCharacters }} characters</h3>
    </div>
    <div class="row text-center justify-content-evenly">
      <CharacterCard
        v-for="character in store.characters"
        class="col-sm-6 col-md-3 col-lg-2"
        :info="character"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.container {
  background-color: white;
}
#chars-founded {
  background-color: black;
  color: white;
}
</style>
