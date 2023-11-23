<script>
export default {
  data() {
    return {
      dcComicsLinks: [
        {
          title: "Characters",
        },
        {
          title: "Comics",
        },
        {
          title: "Movies",
        },
        {
          title: "TV",
        },
        {
          title: "Games",
        },
        {
          title: "Videos",
        },
        {
          title: "News",
        },
      ],
      shopLinks: [
        {
          title: "Shop DC",
        },
        {
          title: "Shop DC Collectibles",
        },
      ],
      dcLinks: [
        {
          title: "Term of Use",
        },
        {
          title: "Privacy policy (New)",
        },
        {
          title: "Add Choices",
        },
        {
          title: "Advertising",
        },
        {
          title: "Jobs",
        },
        {
          title: "Subscriptions",
        },
        {
          title: "Talent Workshop",
        },
        {
          title: "CPSC Certificates",
        },
        {
          title: "Ratings",
        },
        {
          title: "Shop Help",
        },
        {
          title: "Contact Us",
        },
      ],
      sitesLinks: [
        {
          title: "DC",
        },
        {
          title: "MAD Magazine",
        },
        {
          title: "DC Kids",
        },
        {
          title: "DC Universe",
        },
        {
          title: "DC Power Visa",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-top">
    <div class="inner">
      <div class="row">
        <!-- COL Left -->
        <div class="col">
          <div class="dc-comics">
            <ul>
              <h4>DC COMICS</h4>
              <li v-for="item in dcComicsLinks">
                <a href="#">{{ item.title }}</a>
              </li>
            </ul>
          </div>
          <div class="shop margin-top">
            <ul>
              <h4>SHOP</h4>
              <li v-for="item in shopLinks">
                <a href="#">{{ item.title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <!-- // COL Left -->
        <!-- COL Center -->
        <div class="col">
          <div class="dc">
            <ul>
              <h4>DC</h4>
              <li v-for="item in dcLinks">
                <a href="#">{{ item.title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <!-- // COL Center -->
        <!-- COL Right -->
        <div class="col">
          <div class="sites">
            <ul>
              <h4>SITES</h4>
              <li v-for="item in sitesLinks">
                <a href="#">{{ item.title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <!-- // COL Right -->
      </div>
    </div>
    <div class="logo-bg"></div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.footer-top {
  @include flex(space-between, center, row);
  background-image: url(../assets/img/footer-bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  color: white;
  padding-right: 8rem;

  .inner {
    padding-top: 3rem;
    padding-bottom: 3rem;
  }
  .row {
    @include flex(start, start, row);

    .col {
      margin-right: 2rem;
    }

    h4 {
      margin-bottom: 1rem;
    }
    li {
      margin-top: 0.1rem;
      list-style: none;
      a {
        text-decoration: none;
        color: grey;
        font-size: 15px;
      }
    }
  }

  .logo-bg {
    width: 700px;
    height: 500px;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-repeat: no-repeat;
    background-size: cover;

    .div {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
