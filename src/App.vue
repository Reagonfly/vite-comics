<script>
  import AppHeader from './components/AppHeader.vue';
  import ComicsList from './components/ComicsList.vue';
  import AppFooter from './components/AppFooter.vue';
  export default {
    components:{
      AppHeader,
      ComicsList,
      AppFooter
    }
  }
</script>

<template lang="">
  <div>
    <AppHeader />
    <ComicsList />
    <AppFooter />
  </div>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
</style>