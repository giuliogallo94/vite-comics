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
    activeLink: function (activeIndex) {
      {
        this.navItems[activeIndex].isActive = true;
        console.log(this.navItems[activeIndex].isActive);
      }
    },
  },
};
</script>

<template>
  <header>
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo DC" />
    </div>
    <nav>
      <ul>
        <li
          v-for="(link, index) in navItems"
          :key="link.title"
          :class="{ active: link.isActive }"
          @click="activeLink(index)">
          <a href="http://127.0.0.1:5173/">{{ link.title }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

header {
  @include flex();
  padding: 1rem;
  //   height: 150px;
}

nav {
  ul {
    @include flex();
    list-style: none;
    gap: 1.5rem;

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
