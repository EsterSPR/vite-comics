<script>
  import AppHeader from './components/AppHeader.vue';
  import AppFooter from './components/AppFooter.vue';
  import AppComics from './components/AppComics.vue';
  import AppJumbotron from './components/AppJumbotron.vue';

  export default {
    components:{
      AppHeader,
      AppFooter,
      AppComics,
      AppJumbotron
    }
  }
</script>

<template lang="">
  <div>
    <AppHeader />
    <AppJumbotron />
    <AppComics />
    <AppFooter />
  </div>
</template>

<style lang="scss">
  @use './styles/general.scss' as *;
</style>