<script>
export default {
  data() {
    return {
      navItems: [
        {
          title: "CHARACTERS",
          isActive: false,
        },
        {
          title: "COMICS",
          isActive: false,
        },
        {
          title: "MOVIE",
          isActive: false,
        },
        {
          title: "TV",
          isActive: false,
        },
        {
          title: "GAMES",
          isActive: false,
        },
        {
          title: "COLLECTIBLES",
          isActive: false,
        },
        {
          title: "VIDEOS",
          isActive: false,
        },
        {
          title: "FANS",
          isActive: false,
        },
        {
          title: "NEWS",
          isActive: false,
        },
        {
          title: "SHOP",
          isActive: false,
        },
      ],
    };
  },
  methods: {
    activeLink: function (i, activeIndex) {
      {
        for (i = 0; i < this.navItems.length; i++) {
          this.navItems[i].isActive = false;
        }
        this.navItems[activeIndex].isActive = true;
        console.log(this.navItems[activeIndex].isActive);
      }
    },
  },
};
</script>

<template>
  <header>
    <div class="inner">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="Logo DC" />
      </div>
      <nav>
        <ul>
          <li
            v-for="(link, index) in navItems"
            :key="link.title"
            :class="{ active: link.isActive }"
            @click="activeLink(index, index)">
            <a href="#">{{ link.title }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
  .inner {
    @include flex(space-between, center, row);
  }
}

nav {
  ul {
    @include flex(center, center, row);
    list-style: none;
    gap: 1.5rem;
    margin: 0;

    li {
      line-height: 150px;
      border-bottom: 0.5rem solid transparent;
      &.active {
        border-bottom: 0.5rem solid $mainColor;
        a {
          color: $mainColor;
        }
      }
      &:hover {
        border-bottom: 0.5rem solid $mainColor;
        a {
          color: $mainColor;
        }
      }
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}
</style>
