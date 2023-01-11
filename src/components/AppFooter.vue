<script>
export default {
  
}
</script>

<template lang="">
  <footer>
      <div class="footer-shop">
        <div class="footer-container"></div>
      </div>
      <div class="footer-social">
        <div class="footer-container"></div>
      </div>
  </footer>
</template>

<style lang="scss">
  @use '../styles/partials/variables' as * ;
  @use '../styles/partials/mixins' as * ;

  .footer-container{
    @include borderPage;
  }
  .footer-shop{
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    height: 800px;
  }

  
</style>