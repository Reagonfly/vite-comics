<script>
export default {
      data(){
        return{
          imagesBlueSection:[
            {
              image: 'buy-comics-digital-comics.png',
              label: 'Digital Comics'
            },
            {
              image: 'buy-comics-merchandise.png',
              label: 'Merchendise'
            },
            {
              image: 'buy-comics-shop-locator.png',
              label: 'Shop Locator'
            },
            {
              image: 'buy-comics-subscriptions.png',
              label: 'Subscriptions'
            },
            {
              image: 'buy-dc-power-visa.svg',
              label: 'DC Power Visa'
            }
          ],
          socialsLinks:[
            'facebook',
            'twitter',
            'youtube',
            'pinterest',
            'periscope'
          ]
        }
      }
}
</script>

<template lang="">
  <footer>
    <div class="blue-section">
      <div class="container">
        <div class="cols">
          <div v-for="(item, index) in imagesBlueSection" :key="index">
            <img :src="'/img/${item.image}'">
            <span>{{ item.label }}</span>
          </div>
        </div>
      </div>
    </div>
    <div class="main-footer">
      <div class="container">
        <div class="footer-sx">
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
              <li><a href="#">Shop</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
          </div>
          <div class="footer-col">
            <h4>DC</h4>
            <ul>
              <li><a href="#">Terms of Use</a></li>
              <li><a href="#">Privacy Policy (New)</a></li>
              <li><a href="#">Ad Choices</a></li>
              <li><a href="#">Advertising</a></li>
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
              <li><a href="#">CDC Universe</a></li>
              <li><a href="#">DC Pover Visa</a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <div class="social">
        <div class="col-but">
          <button class="footer-button">Sign-up now!</button>
        </div>
        <div class="icon">
          <h3 class="follow">Follow us</h3>
          <ul>
            <li v-for="(item, index) in socialsLinks" :key="index">
              <a href="#"><img :src="'/img/${item.image}'" :alt="logo-social"></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/variables' as *;
  @use '../styles/partials/mixins' as *;

  .blue-section{
    background-color: $primary-color;
    padding: 3rem;
    
    .cols{
      @include flex-center;
      justify-content: space-between;

      img{
        width: 75px;
        vertical-align: middle;
        padding: 10px;
      }
  
      span{
        text-transform: uppercase;
        color: white;
      }
    }
  }

  .main-footer{
    background-image: url('/img/footer-bg.jpg');
    background-size: cover;

    .container{
      display: flex;
      background-image: url('/img/dc-logo-bg.png');
      background-position: right center;
      background-repeat: no-repeat;

      .footer-sx{
        display: flex;
        width: 30%;
      }
      
      .footer-col{
        color: $color-white;
        margin: 3rem 0;

        h4{
          text-transform: uppercase;
        }

        ul{
          list-style: none;
          padding-bottom: 10px;
          li{
            padding: 5px 0;
            a{
              color: gray;
              font-size: 15px;
            }
          }
        }
      }
    }
  }

  .bottom-footer{
    background-color: #303030;
    display: flex;
    justify-content: space-around;

    .social {
    height: 80px;
    background-color: #303030;
    align-items: center;
    display: flex;
    justify-content: space-between;

    .footer-button {
    background-color: #303030;
    border: 3px solid rgb(35, 56, 219);
    color: white;
    font-weight: bold;
    text-transform: uppercase;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    font-size: 12px;
    cursor: pointer;
    }

    .icon {
        display: flex;
        align-items: center;
        margin-left: 20rem;

        ul {
            display: flex;
            gap: .5em;
        }

        li {
            display: flex;
            color: $color-white;
            list-style-type: none;
            &:hover {
                filter: brightness(100);
            }
        }
        .follow {
            color: #0282f9;
            padding-right: .5em;
        }
      }
    }
  }

</style>
