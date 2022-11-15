<script>
export default {
  name: 'AppMain'
}
</script>

<template>
  
  <main>
    <div class="container">
      <p> --> Content goes here</p>
    </div>
  </main>

</template>

<style lang="scss" scoped>

  @use '../style/partials/mixin' as *;
  @use '../style/partials/variables' as *;

  main {
    height: $header-height;
    background-color: $secondary-color;
    font-size: 1.5rem;
    color: $text-light;
    font-weight: bold;
    @include dFlexRow(alignCenter);
  }

</style>