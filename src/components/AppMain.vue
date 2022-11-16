<script>

import CardProduct from './CardProduct.vue'; 

import dcComics from '../data/dc-comics';

export default {

  name: 'AppMain',

  components: {

    CardProduct

  },

  data(){
    return{

      dcComics,
      title: 'Current series',

    }
  },

}

</script>

<template>
  
  <main>
    <div class="container">

      <h2>{{title}}</h2>

      <div class="card">

        <CardProduct
          v-for="(comic, index) in dcComics" :key="index" 
          :img="comic.thumb"
          :text="comic.series"
        />

      </div>

      <div class="button">
        <button>Load more</button>
      </div>
      
    </div>
  </main>

</template>

<style lang="scss" scoped>

  @use '../style/partials/mixin' as *;
  @use '../style/partials/variables' as *;

  main {
    background-color: $secondary-color;
    .container {
      padding: 50px 0 20px;
      position: relative;
      h2 {
        @include boxRectangleText(title);
        position: absolute;
        top: -30px;
      }
      .card {
        @include dFlexRow(wrap);
      }
      .button {
        text-align: center;
        button {
          @include boxRectangleText(btnSmall);
        }
      }
    }
    
  }

</style>