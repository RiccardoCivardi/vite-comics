<script>

import MenuList from './MenuList.vue';
import AppFooterSocial from './AppFooterSocial.vue';

import {dcComicsMenu, shopMenu, DcMenu, SitesMenu} from '../data/menu';

export default {

  name: 'AppFooter',

  components: {

    MenuList,
    AppFooterSocial,

  },

  data(){
    return{

      dcComicsMenu,

      shopMenu,

      DcMenu,

      SitesMenu

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
          <MenuList :objectMenu="dcComicsMenu" />
          <h3>Shop</h3>
          <MenuList :objectMenu="shopMenu" />
        </div>

        <div class="col">
          <h3>Dc</h3>
          <MenuList :objectMenu="DcMenu" />
        </div>

        <div class="col">
          <h3>Sites</h3>
          <MenuList :objectMenu="SitesMenu" />
        </div>

      </nav>

    </div> 
   
    <AppFooterSocial/>

  </footer>

</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;

footer{
  height: $footer-height;
  background-image: url('../assets/img/footer-bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  .container {
    height: 100%;
    height: calc($footer-height - $social-footer-height);
    background-image: url('../assets/img/dc-logo-bg.png');
    background-repeat: no-repeat;
    background-position: right;
    .footer-menu {
      display: flex;
      padding: 40px 0;
      .col {
        margin-right: 30px;
        h3 {
          color: $text-light;
          text-transform: uppercase;
        }
      }
    }  
  } 
}

</style>