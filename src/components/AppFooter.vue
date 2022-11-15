<script>

import AppFooterSocial from './AppFooterSocial.vue';

export default {

  name: 'AppFooter',

  components: {
    AppFooterSocial
  },

  data(){
    return{

      dcComicsMenu:[
        {
          text: 'Characters',
          href: '#'
        },
        {
          text: 'Comics',
          href: '#'
        },
        {
          text: 'Movies',
          href: '#'
        },
        {
          text: 'TV',
          href: '#'
        },
        {
          text: 'Games',
          href: '#'
        },
        {
          text: 'Videos',
          href: '#'
        },
        {
          text: 'News',
          href: '#'
        }
      ],

      shopMenu: [
        {
          text: 'Shop DC',
          href: '#'
        },
        {
          text: 'Shop DC Collectibles',
          href: '#'
        }
      ],

      DcMenu: [
        {
          text: 'Terms of Use',
          href: '#'
        },
        {
          text: 'Privacy policy(New)',
          href: '#'
        },
        {
          text: 'Ad Choices',
          href: '#'
        },
        {
          text: 'Advertising',
          href: '#'
        },
        {
          text: 'Jobs',
          href: '#'
        },
        {
          text: 'Subscriptions',
          href: '#'
        },
        {
          text: 'Talent Workshop',
          href: '#'
        },
        {
          text: 'CPSC Certificates',
          href: '#'
        },
        {
          text: 'Ratings',
          href: '#'
        },
        {
          text: 'Shop Help',
          href: '#'
        },
        {
          text: 'Contact Us',
          href: '#'
        }
      ],

      SitesMenu: [
        {
          text: 'DC',
          href: '#'
        },
        {
          text: 'MAD Magazine',
          href: '#'
        },
        {
          text: 'DC kids',
          href: '#'
        },
        {
          text: 'DC Universe',
          href: '#'
        },
        {
          text: 'DC Power Visa',
          href: '#'
        }
      ]

    }
  }

}

</script>

<template>

  <footer>

    <div class="container">
    
      <nav class="footer-menu">

        <div class="col">
          <h3>Dc comics</h3>
          <ul>
            <li v-for="(link, index) in dcComicsMenu" :key="index"><a href="link.href">{{link.text}}</a></li>
          </ul>
          <h3>Shop</h3>
          <ul>
            <li v-for="(link, index) in shopMenu" :key="index"><a href="link.href">{{link.text}}</a></li>
          </ul>
        </div>

        <div class="col">
          <h3>Dc</h3>
          <ul>
            <li v-for="(link, index) in  DcMenu" :key="index"><a href="link.href">{{link.text}}</a></li>
          </ul>
        </div>

        <div class="col">
          <h3>Sites</h3>
          <ul>
            <li v-for="(link, index) in  SitesMenu" :key="index"><a href="link.href">{{link.text}}</a></li>
          </ul>
        </div>

      </nav>

      <div class="image">
        <img src="../assets/img/dc-logo-bg.png" alt="Logo DC">
      </div>

    </div> 
   
    <AppFooterSocial/>

  </footer>

</template>

<style lang="scss" scoped>

@use '../style/partials/mixin' as *;
@use '../style/partials/variables' as *;

footer{
  height: $footer-height;
  height: calc($footer-height - $social-footer-height);
  background-image: url('../assets/img/footer-bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  .container {
    height: 100%;
    @include dFlexRow(between);
    .footer-menu {
      display: flex;
      padding: 40px 0;
      .col {
        margin-right: 30px;
        h3 {
          color: $text-light;
          text-transform: uppercase;
        }
        h3, ul {
          margin-bottom: 15px;
        }
        li {
          margin-bottom: 5px;
          a {
            text-decoration: none;
            color: lighten($bg-dark, 40%);
            font-size: 0.8rem;
          }
        }
      }
    }  
    .image {
      width: 560px;
      height: 100%;
      overflow: hidden;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  } 
}

</style>