<script>
export default {
  props: {
    info: Object,
  },
};
</script>

<template>
  <section class="g-4 mx-3 py-3">
    <img :src="info.img" :alt="info.name" />
    <h5 class="py-3">{{ info.name }}</h5>
    <div class="series">{{ info.category }}</div>
    <div class="status">{{ info.status }}</div>
  </section>
</template>

<style lang="scss" scoped>
section {
  background-color: #2e3a46;
  color: white;
}
img {
  width: 100%;
  height: 15.9375rem;
  object-fit: cover;
}

.series,
.status {
  color: grey;
}
</style>
