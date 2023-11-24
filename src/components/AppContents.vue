<script>
import AppCards from "./AppCards.vue";
export default {
  components: {
    AppCards,
  },
  data() {
    return {
      cardsDcArray: series,
    };
  },
};
</script>

<template>
  <section class="content">
    <div class="content-img"></div>
    <div class="inner">
      <div class="content-title">
        <span>CURRENT SERIES</span>
      </div>
      <div class="row">
        <AppCards
          v-for="value in cardsDcArray"
          :title="value.series.toUpperCase()"
          :imageName="value.thumb" />
      </div>
      <div class="load">
        <button>LOAD MORE</button>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.content {
  background-color: #1c1c1c;

  .content-img {
    min-height: 400px;
    background-image: url(../assets/img/jumbotron.jpg);
  }

  .inner {
    .content-title {
      span {
        background-color: $mainColor;
        padding: 1rem;
        color: white;
        font-weight: bold;
      }
    }

    .row {
      padding-top: 2rem;
      display: flex;
      flex-wrap: wrap;
    }

    .load {
      text-align: center;
      padding: 2rem;

      button {
        padding: 0.6rem 3rem;
        background-color: $mainColor;
        border: none;
        color: white;
        font-weight: bold;
      }
    }
  }
}
</style>
