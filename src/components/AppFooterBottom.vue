<script>
export default {
  data() {
    return {
      socialLogos: [
        {
          title: "Facebook",
          url: "footer-facebook.png",
        },
        {
          title: "Twitter",
          url: "footer-twitter.png",
        },
        {
          title: "YouTube",
          url: "footer-youtube.png",
        },
        {
          title: "Pinterest",
          url: "footer-pinterest.png",
        },
        {
          title: "Periscope",
          url: "footer-periscope.png",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-bottom">
    <div class="inner">
      <div class="sign-up">
        <button>SIGN-UP NOW!</button>
      </div>

      <div class="social-media">
        <h4>FOLLOW US</h4>
        <div v-for="item in socialLogos" class="social-logo">
          <img :src="`./src/assets/img/${item.url}`" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.footer-bottom {
  background-color: #303030;
  padding: 2rem;

  .inner {
    @include flex(space-between, center, row);
    button {
      padding: 0.5rem;
      background-color: #303030;
      border: 1px solid $mainColor;
      color: white;
    }
    .social-media {
      @include flex(space-between, center, row);
      gap: 1rem;
      h4 {
        color: $mainColor;
      }
      .social-logo {
        color: white;
      }
    }
  }
}
</style>
