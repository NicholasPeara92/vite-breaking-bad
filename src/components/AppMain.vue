<script>
import SelectCategory from "./SelectCategory.vue";
import CharactersSection from "./CharactersSection.vue";
import CharacterCard from "./CharacterCard.vue";

export default {
  components: {
    SelectCategory,
    CharactersSection,
    CharacterCard,
  },
};
</script>

<template>
  <SelectCategory />
  <CharactersSection />
  <CharacterCard />
</template>

<style lang="scss" scoped></style>
