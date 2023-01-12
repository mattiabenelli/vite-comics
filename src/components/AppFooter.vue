<script>
export default {
  data() {
    return {
      socialsLink:[
        'facebook',
        'twitter',
        'youtube',
        'pinterest',
        'periscope',
      ],
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
          <div class="blue-section-links" v-for="(item,index) in imagesBlueSection" :key="index">
            <img :src="`/img/${item.image}`" alt="">
            <div class="blue-section-links-text">{{ item.label }}</div>
          </div>
        </div>
      </div>
      <div class="footer-shop">
        <div class="footer-container">
          <div class="footer-sx-jumbo">
            <div class="footer-col">
            <h4>DC COMICS</h4>
            <ul>
              <li><a href="#">Characters</a></li>
              <li><a href="#">Comics</a></li>
              <li><a href="#">Movies</a></li>
              <li><a href="#">TV</a></li>
              <li><a href="#">Games</a></li>
              <li><a href="#">Videos</a></li>
              <li><a href="#">News</a></li>
            </ul>
            <h4>SHOP</h4>
              <ul>
                <li><a href="#">Shop DC</a></li>
                <li><a href="#">Shop DC Collectibles</a></li>
              </ul>
            </div>
            <div class="footer-col">
              <h4>DC</h4>
                <ul>
                  <li><a href="#">Terms Of Use</a></li>
                  <li><a href="#">Privacy policy (New)</a></li>
                  <li><a href="#">Ad Choices</a></li>
                  <li><a href="#">Advertings</a></li>
                  <li><a href="#">Jobs</a></li>
                  <li><a href="#">Subscriptions</a></li>
                  <li><a href="#">Talent Workshops</a></li>
                  <li><a href="#">CPSC Certificates</a></li>
                  <li><a href="#">Ratings</a></li>
                  <li><a href="#">Shop Help</a></li>
                  <li><a href="#">Contact Us</a></li>
                </ul>
            </div>
            <div class="footer-col">
              <h4>Sites</h4>
                <ul>
                  <li><a href="#">DC</a></li>
                  <li><a href="#">MAD Magazine</a></li>
                  <li><a href="#">DC Kids</a></li>
                  <li><a href="#">DC Universe</a></li>
                  <li><a href="#">DC Power Visa</a></li>
                </ul>
            </div>
          </div>
          <div class="footer-dx-jumbo">
            <img src="/img/dc-logo-bg.png" alt="">
          </div>
        </div>

      </div>
      <div class="footer-social">
        <div class="footer-container">
          <div class="row">
            <div class="footer-sx">
            <button>SIGN-UP NOW!</button>
          </div>
          <div class="footer-dx">
            <div class="follow">FOLLOW US</div>
            <div class="icons">
              <div class="icon">
                <img src="/img/footer-facebook.png" alt="">
              </div>
              <div class="icon">
                <img src="/img/footer-twitter.png" alt="">
              </div>
              <div class="icon">
                <img src="/img/footer-youtube.png" alt="">
              </div>
              <div class="icon">
                <img src="/img/footer-pinterest.png" alt="">
              </div>
              <div class="icon">
                <img src="/img/footer-periscope.png" alt="">
              </div>
            </div>
          </div>
          </div>
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
  }
  .footer-sx-jumbo{
    display: flex;
    width: 30%;
  }
  .footer-dx-jumbo{
    img{
      height: 570px;
    }
    display: flex;
    width: 70%;
    justify-content: flex-end;
    align-items: center;
    height: 450px;
  }
  .footer-col{
    color: white;
    padding: 0 20px;
    h4{
      padding: 10px 0;
    }
    ul{
      list-style: none;
      li{
        padding: 5px 0;
        list-style-type: none;
        a{
          text-decoration: none;
          color: gray
        }
      }
    }
  }
  .footer-container{
        @include flex-align;
        justify-content:space-between;
  }
  .footer-social{
    padding: 20px 0;
    position: relative;
    z-index: 1;
    background-color: #303030;
    height: 100%;
      button{
            border: 1px solid $DCblue;
            background-color: transparent;
            color: white;
            font-size: 15px;
            padding: 15px 20px;
      }
      .row{
        width: 100%;
        flex-wrap: nowrap
      }
      .footer-sx{
        width: 100%
      }
      .footer-dx{
        @include flex-align;
        justify-content: flex-end;
        width: 100%;
          .follow{
            color: $DCblue;
            font-size: 20px;
            margin-right: 30px;
          }
          .icons{
            display: flex;
            justify-content: space-evenly;
            gap: 20px;
          }
      }
  }
  .blue-section{
    background-color: $DCblue;
    padding: 40px 0;
    position: relative;
    z-index: 1;
      
      .blue-section-links{
        @include flex-align;
        color: white;
          img{
            height: 100px;
          }
      }
      .blue-section-links-text{
        padding-left: 10px;
      }
  }

  
</style>