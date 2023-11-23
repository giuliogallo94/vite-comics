<script>
import AppHeader from "./components/AppHeader.vue";
import AppContents from "./components/AppContents.vue";
import AppShopping from "./components/AppShopping.vue";
import AppFooterTop from "./components/AppFooterTop.vue";
import AppFooterBottom from "./components/AppFooterBottom.vue";

export default {
  components: {
    AppHeader,
    AppContents,
    AppShopping,
    AppFooterTop,
    AppFooterBottom,
  },
};
</script>

<template>
  <AppHeader />
  <AppContents />
  <AppShopping />
  <footer>
    <AppFooterTop />
    <AppFooterBottom />
  </footer>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
