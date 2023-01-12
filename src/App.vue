<script>
  import AppHeader from './components/AppHeader.vue'
  import AppFooter from './components/AppFooter.vue'
  import AppContent from './components/AppContent.vue'
  import ComicCard from './components/ComicCard.vue'
  
  export default{
    components:{
      AppHeader,
      AppFooter,
      AppContent,
      ComicCard,
    },
  }
</script>

<template lang="">
  <AppHeader></AppHeader>
  <AppContent></AppContent>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *
</style>

