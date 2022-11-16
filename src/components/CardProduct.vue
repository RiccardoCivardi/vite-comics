<script>

export default {

  name: 'CardProduct',

  props: {

    img: String,
    text: String

  }

}

</script>

<template>

  <div class="card">
    <div class="image">
      <img :src="img" alt="text">
    </div>

    <h4>{{text}}</h4>

  </div>
  
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;

.card {
  flex-basis: calc(100% / 6);
  padding: 15px;
  .image {
    width: 100%;
    margin-bottom: 15px;
    img {
      aspect-ratio: 1/1;
      object-fit: cover;
      object-position: top;
    }
  }
  h4 {
    font-weight: 400;
    text-transform: uppercase;
    color: $text-light;
  }
}

</style>