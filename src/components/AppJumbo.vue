<script>
export default {

  name: 'AppJumbo'

}
</script>

<template>

  <div class="jumbotron">
    <img src="../assets/img/jumbotron.jpg" alt="Jumbo comics">
  </div>
  
</template>

<style lang="scss" scoped> 

@use '../style/partials/variables' as *;

.jumbotron {
  height: $jumbo-height;
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
  }
}

</style>