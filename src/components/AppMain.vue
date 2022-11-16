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

      dcComics

    }
  }

}

</script>

<template>
  
  <main>
    <div class="container">
      
      <CardProduct
        v-for="(comic, index) in dcComics" :key="index" 
        :img="comic.thumb"
        :text="comic.series"
      />

    </div>
  </main>

</template>

<style lang="scss" scoped>

  @use '../style/partials/mixin' as *;
  @use '../style/partials/variables' as *;

  main {
    background-color: $secondary-color;
    .container {
      @include dFlexRow(wrap);

    }
    
  }

</style>