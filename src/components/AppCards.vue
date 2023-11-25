<script>
export default {
  props: {
    title: String,
    imageName: String,
    indexCard: Number,
  },
};
</script>

<template>
  <div class="ms_card">
    <img
      :src="imageName"
      :alt="title"
      data-bs-toggle="modal"
      :data-bs-target="`#exampleModal${indexCard}`" />
    <span>{{ title }}</span>
  </div>
</template>

<style lang="scss" scoped>
.ms_card {
  width: calc(100% / 6);
  padding: 1rem;
  img {
    width: 100%;
    height: 300px;
  }

  span {
    font-size: 15px;
    font-weight: bold;
    color: white;
  }
}
</style>
