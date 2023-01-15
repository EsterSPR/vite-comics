<script>
export default {
  data(){
    return{
      footerIcons:[
        {
          icon: '../public/img/buy-comics-digital-comics.png',
          text: 'DIGITAL COMICS',
        },
        {
          icon: '../public/img/buy-comics-merchandise.png',
          text: 'DC MERCHANDISE',
        },
        {
          icon: '../public/img/buy-comics-subscriptions.png',
          text: 'SUBSCRIPTION',
        },
        {
          icon: '../public/img/buy-comics-shop-locator.png',
          text: 'COMIC SHOP LOCATOR',
        },
        {
          icon: '../public/img/buy-dc-power-visa.svg',
          text: 'DC POWER VISA',
        }
      ],
      socialIcons:[
        {
            icon: '../public/img/footer-facebook.png',
            link: '#',
        },
        {
            icon: '../public/img/footer-twitter.png',
            link: '#',
        },
        {
            icon: '../public/img/footer-youtube.png',
            link: '#',
        },
        {
            icon: '../public/img/footer-pinterest.png',
            link: '#',
        },
        {
            icon: '../public/img/footer-periscope.png',
            link: '#',
        },
      ]
    }
  }
}
</script>

<template lang="">
  <footer>
    <div class="footer-top">
      <ul class="icon-list">
        <li v-for="(icons, index) in footerIcons" :key="index">
          <img :src="icons.icon" :alt="icons.text">
          <p>{{icons.text}}</p>
        </li>
      </ul>
    </div>
    <div class="footer-main">
      <div class="footer-list">
        <div class="list-flex">
          <ul>
            <li><h3>DC COMICS</h3></li>
            <li><a href="#">Characters</a></li>
            <li><a href="#">Comics</a></li>
            <li><a href="#">Movies</a></li>
            <li><a href="#">TV</a></li>
            <li><a href="#">Games</a></li>
            <li><a href="#">Videos</a></li>
            <li><a href="#">News</a></li>
          </ul>
          <ul>
            <li><h3>SHOP</h3></li>
            <li><a href="#">Shop DC</a></li>
            <li><a href="#">Shop DC Collectibles</a></li>
          </ul>
        </div>
        <div class="list-flex">
          <ul>
            <li><h3>DC</h3></li>
            <li><a href="#">Terms of Use</a></li>
            <li><a href="#">Privacy policy (New)</a></li>
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
        <div class="list-flex">
          <ul>
            <li><h3>SITES</h3></li>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD Magazine</a></li>
            <li><a href="#">DC Kids</a></li>
            <li><a href="#">DC Universe</a></li>
            <li><a href="#">DC Power Visa</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-img">
        <img src="../../public/img/dc-logo-bg.png">
      </div>
    </div>
    <div class="footer-bottom">
      <div class="sign-up">
        <a href="#"><button id="sign-up-btn">SIGN-UP NOW!</button></a>
      </div>
      <div class="social-container">
        <p>FOLLOW US</p>
        <ul>
          <li v-for="(social, index) in socialIcons" :key="index">
              <a :href="social.link"><img :src="social.icon"></a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
  @use '../styles/singles/variables' as *;
  
  footer{
    color: $dc-white;
    font-family: 'Roboto', sans-serif;
    font-weight: 300;

    .footer-top, .footer-main, .footer-bottom{
      width: 100vw;
    }

    .footer-top{
      background-color: $dc-blue;
      padding: 50px 10%;
      margin-top: 120px; /**********REMOVE AND PUT IN MAIN**********/

      .icon-list{
        list-style: none;
        display: flex;
        justify-content: space-between;
      }

      .icon-list li{
        display: flex;
        align-items: center;
      }

      .icon-list img{
        width: 50px;
        margin-right: 10px;
      }
    }

    .footer-main{
      background-image: url('../../public/img/footer-bg.jpg');
      background-size: cover;
      padding: 0px 10%;
      display: flex;
      justify-content: space-between;
      overflow: hidden;

      .footer-img{
        margin: -100px 0;
      }
      .footer-list{
        display: flex;
        margin: 50px 0;
        color: rgba(255, 255, 255, 0.5);
      }
      .footer-list ul{
        list-style-type: none;
        margin-bottom: 20px;
        margin-right: 30px;
      }
      .footer-list h3{
        font-family: 'Roboto Condensed', sans-serif;
        margin-bottom: 5px;
        color: rgba(255, 255, 255, 1);
      }
    }

    .footer-bottom{
      background-color: $dc-grey;
      display: flex;
      justify-content: space-between;
      padding: 25px 10%;

      #sign-up-btn{
        border: 2px solid $dc-blue;
        padding: 10px;
        background-color: $dc-grey;
        color: $dc-white;
        font-weight: bold;
        transition: background-color 0.1s;
      }
      #sign-up-btn:hover{
        cursor: pointer;
        background-color: $dc-blue;
      }
      .social-container{
        display: flex;
        align-items: center;
      }
      .social-container p{
        color: $dc-blue;
        font-weight: bold;
        font-family: 'Roboto Condensed', sans-serif;
        font-weight: bold;
        font-size: 14pt;
      }
      .social-container ul{
        list-style-type: none;
        display: flex;
      }
      .social-container img{
        width: 30px;
        margin-left: 20px;
      }
    }
  }
</style>