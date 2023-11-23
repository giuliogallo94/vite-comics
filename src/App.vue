<script>
import AppHeader from "./components/AppHeader.vue";
import AppContents from "./components/AppContents.vue";
export default {
  components: {
    AppHeader,
    AppContents,
  },
};
</script>

<template>
  <AppHeader />
  <AppContents />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
