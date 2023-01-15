<script>
export default {
  data(){
    return{
      footerIcon:[
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
        'facebook',
        'twitter',
        'youTube',
        'pinterest',
        'periscope'
      ]
    }
  }
}
</script>

<template lang="">
  <footer>
    <div class="footer-top">
      <ul class="icon-list">
        <li v-for="(icons, index) in footerIcon" :key="index">
          <img :src="icons.icon" :alt="icons.text">
          <p>{{icons.text}}</p>
        </li>
      </ul>
    </div>
    <div class="footer-main"></div>
    <div class="footer-bottom"></div>
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
      padding: 50px 10%;
    }

    .footer-top{
      background-color: $dc-blue;
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
    }

    .footer-bottom{
      background-color: #303030;
    }
  }
</style>