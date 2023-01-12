<script>
import ComicCard from './ComicCard.vue';
import ComicsContent from '../assets/data/ComicsContent.js';

export default{
  components:{
    ComicCard,
  },
  data() {
    return {
      products: ComicsContent,
    }
  }  
}

</script>
<template lang="">
  <main>
    <div class="main-container">
      <div class="row">
        <ComicCard v-for="(item,index) in products" :key="index" :comic="item"></ComicCard>
      </div>
    </div>
  </main>
</template>

<style lang="scss">
  @use '../styles/partials/variables' as * ;
  @use '../styles/partials/mixins' as * ;

  
  .main-container{
    @include borderPage;
  }
  .row {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: space-between;
}
main{
  background-color: #1C1C1C;
  color: white;
  padding: 20px 0px;
}
</style>