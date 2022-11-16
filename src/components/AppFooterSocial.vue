<script>

import socialIcons from '../data/social';
import {getImagePath} from '../data/methods';

export default {

  name: 'AppFooterSocial',

  data(){
    return{

      socialIcons,
      getImagePath

    }
  },

}

</script>

<template>

  <div class="social-footer">
    <div class="container">
      <div class="sign-up">
        <a href="">Sign up now!</a>
      </div>
      <div class="social">
        <span>Follow us</span>
        <a
          v-for="(icon, index) in socialIcons"
          :key="index" 
          href="">
            <img :src="getImagePath(icon.name)" :alt="icon.alt">
        </a>
      </div>
    </div>  
  </div>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/mixin' as *;
@use '../style/partials/variables' as *;

.social-footer {
  height: $social-footer-height;
  background-color: $bg-dark;
  .container{
    height: 100%;
    @include dFlexRow(betweenCenter);
    .sign-up {
      border: 2px solid $primary-color;
      padding: 10px;
      cursor: pointer;
      transition: all 1s;
      a {
        font-size: 1.3rem;
        font-weight: 500;
        color: $text-light;
        text-transform: uppercase;
        text-decoration: none;
      }
      &:hover {
        background-color: $primary-color;
      }
    }
    .social {
      @include dFlexRow(alignCenter);
      * {
        margin: 0 5px;
      }
      span {
      font-size: 1.5rem;
      text-transform: uppercase;
      font-weight: bold;
      color: $primary-color;
      }
      img:hover {
        filter: brightness(2);
      }
    }
  }
}

</style>