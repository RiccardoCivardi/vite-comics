<script>

import {menu} from '../data/menu';

export default {
 
  name: 'AppHeader',

  data(){
    return{

      menu
      
    }
  }

}

</script>

<template>

  <header>

    <div class="container">

      <div class="logo">
        <img src="/img/dc-logo.png" alt="Logo DC">
      </div>
  
      <nav>
        <ul>
          <li
            v-for="(link, index) in menu" 
            :key="index"
            :class="{'active': link.current}">
            <a :href="link.href">{{link.text}}</a>
          </li>
        </ul>
      </nav>

    </div>

  </header>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/mixin' as *;
@use '../style/partials/variables' as *;

header {
  height: $header-height;
  .container {
    height: 100%;
    @include dFlexRow(between);
    * {
      cursor: pointer;
    }
    .logo {
      width: 90px;
      @include dFlexRow(alignCenter)
    }
    nav, ul, li {
      height: 100%;
    }
    ul {
      li {
        line-height: $header-height;
        display: inline-block;
        margin: 0 10px;
        a {
          text-decoration: none;
          text-transform: uppercase;
          font-weight: 500;
          color: $secondary-color;
        }
        &:hover,
        &.active {
          border-bottom: 5px solid $primary-color;
        }
        &:hover a,
        &.active a{
          color: $primary-color;
        }
      }
    }
  }

}

</style>