<script>
  import AppFooter from './components/AppFooter.vue';
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppSection from './components/AppSection.vue';
  export default {
    components: {
      AppHeader,
      AppMain,
      AppSection,
      AppFooter,
    }
  }
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppSection />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
