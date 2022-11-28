<script>
import axios from "axios";
import CharacterCard from "./CharacterCard.vue";

export default {
  components: {
    CharacterCard,
  },
  data() {
    return {
      characters: [],
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.characters = resp.data;
      console.log(resp);
    });
  },
};
</script>

<template>
  <section class="container p-5">
    <div id="chars-founded" class="p-3">Fount 62 characters</div>
    <div class="row text-center justify-content-evenly">
      <CharacterCard
        v-for="character in characters"
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
