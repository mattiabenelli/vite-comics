<script>
export default {
  data() {
    return {
      imagesBlueSection:[
        {
          image: 'buy-comics-digital-comics.png',
          label: 'DIGITAL COMICS'
        },
        {
          image: 'buy-comics-merchandise.png',
          label: 'DC MERCHANDISE'
        },
        {
          image: 'buy-comics-shop-locator.png',
          label: 'COMIC SHOP LOCATOR'
        },
        {
          image: 'buy-comics-subscriptions.png',
          label: 'SUBSCRIPTION'
        },
        {
          image: 'buy-dc-power-visa.svg',
          label: 'DC POWER VISA',
        }
      ]
    }
  }
}
</script>

<template lang="">
  <footer>
      <div class="blue-section">
        <div class="footer-container">
          <div v-for="(item,index) in ImagesBlueSection" :key="index">
            <img :src="`/img/${item.image}`" alt="">
          </div>
        </div>
      </div>
      <div class="footer-shop">
        <div class="footer-container">
          
        </div>
      </div>
      <div class="footer-social">
        <div class="footer-container">

        </div>
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
    background-image: url('/img/footer-bg.jpg');
    background-size: cover;
    height: 800px;
  }

  
</style>