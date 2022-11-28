<script>
import Appheader from "./components/Appheader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  components: {
    Appheader,
    AppMain,
  },
};
</script>

<template>
  <div class="background">
    <Appheader />
    <AppMain />
  </div>
</template>

<style lang="scss">
@import "./style/global.scss";

.background {
  background-color: #2e3a46;
}
</style>
