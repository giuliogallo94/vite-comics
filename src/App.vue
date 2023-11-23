<script>
import AppHeader from "./components/AppHeader.vue";
import AppContents from "./components/AppContents.vue";
import AppShopping from "./components/AppShopping.vue";
export default {
  components: {
    AppHeader,
    AppContents,
    AppShopping,
  },
};
</script>

<template>
  <AppHeader />
  <AppContents />
  <AppShopping />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
