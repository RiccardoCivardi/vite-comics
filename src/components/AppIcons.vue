<script>

import {getImagePath} from '../data/methods';

export default {
 
  name: 'AppIcons',

  data(){
    return {

      getImagePath,

      icons: [
        {
          name: 'buy-comics-digital-comics.png',
          text: 'Digital comics'
        },
        {
          name: 'buy-comics-merchandise.png',
          text: 'Dc merchandaise'
        },
        {
          name: 'buy-comics-subscriptions.png',
          text: 'Subscription'
        },
        {
          name: 'buy-comics-shop-locator.png',
          text: 'Comic shop locator'
        },
        {
          name: 'buy-dc-power-visa.svg',
          text: 'Dc power visa'
        }
      ]

    }
  }

}

</script>

<template>
  
  <div class="icons-container">
    <div class="container">
      
      <div 
        v-for="(icon, index) in icons"
        :key="index"
        class="icon">
        <div class="image">
          <img :src="getImagePath(icon.name)" :alt="`${icon.text} picture`">
        </div>
        <div class="text">
          <span>{{icon.text}}</span>
        </div>
      </div>
      
    </div>
  </div>
 

</template>

<style lang="scss" scoped>

@use '../style/partials/mixin' as *;
@use '../style/partials/variables' as *;

.icons-container {
  height: $icons-height;
  background-color: $primary-color;
  .container{
    height: 100%;
    @include dFlexRow(aroundCenter);
    .icon {
      @include dFlexRow();
      .image {
        width: 45px;
        height: 60px;
        margin-right: 10px;
        img {
          width: 100%;
          height: 100%;
          object-fit: contain;
        }
      }
      .text {
        text-transform: uppercase;
        color: $text-light;
        font-size: 1.1rem;
      }
    }
  }
}

</style>