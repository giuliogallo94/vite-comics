<script>
export default {
  props: {
    title: String,
    imageName: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="imageName" :alt="title" />
    <h5>{{ title }}</h5>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: calc(100% / 6);
  padding: 1rem;
  img {
    width: 100%;
    height: 300px;
  }

  h5 {
    color: white;
  }
}
</style>
