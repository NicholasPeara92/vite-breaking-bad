<script>
import CharacterCard from "./CharacterCard.vue";

export default {
  components: {
    CharacterCard,
  },
};
</script>

<template>
  <section class="container p-5">
    <div id="chars-founded" class="p-3">Fount 62 characters</div>
    <div class="row">
      <CharacterCard />
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
