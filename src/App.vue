<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
}

</script>

<template>

  <AppHeader />
  <AppMain />
  <AppFooter />

</template>

<style lang="scss">
@use "./styles/partials/variables" as*;
@use "./styles/partials/mixins" as*;
@use "./styles/general.scss" as*;

.container {
  max-width: 1200px;
  margin: 0 auto;
}
</style>
