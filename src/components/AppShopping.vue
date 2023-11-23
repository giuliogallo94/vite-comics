<script>
export default {
  data() {
    return {
      buyItem: [
        {
          title: "DIGITAL COMICS",
          url: "buy-comics-digital-comics.png",
        },
        {
          title: "DC MERCHANDISE",
          url: "buy-comics-merchandise.png",
        },
        {
          title: "SUBSCRIPTION",
          url: "buy-comics-shop-locator.png",
        },
        {
          title: "COMIC SHOP LOCATOR",
          url: "buy-comics-subscriptions.png",
        },
        {
          title: "DC POWER VISA",
          url: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<template>
  <section class="shopping">
    <div class="inner">
      <div class="inner-shopping">
        <div
          v-for="(item, index) in buyItem"
          :key="item"
          class="inner-shopping-item">
          <div class="buy-img">
            <img :src="`./src/assets/img/${item.url}`" alt="" />
          </div>
          <div class="buy-title">
            <h5>
              {{ item.title }}
            </h5>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.shopping {
  background-color: $mainColor;
  height: 200px;

  .inner-shopping {
    padding: 0 2rem;
    color: white;
    height: 100%;
    @include flex(space-between, center, row);

    .inner-shopping-item {
      @include flex(center, center, row);
      .buy-img {
        margin-right: 0.5rem;
        img {
          width: 65px;
          height: 70px;
        }
      }
    }
  }
}
</style>
