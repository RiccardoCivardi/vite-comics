<script>
export default {

  name: 'MenuList',

  props: {

    objectMenu: Object,
    
  }
  
}
</script>

<template>

  <ul>
    <li v-for="(link, index) in objectMenu" :key="index"><a href="link.href">{{link.text}}</a></li>
  </ul>
  
</template>


<style lang="scss" scoped>

@use '../style/partials/variables' as *;

ul {
  margin: 15px 0;
  li {
    margin-bottom: 5px;
    a {
      text-decoration: none;
      color: lighten($bg-dark, 40%);
      font-size: 0.8rem;
    }
  }
}

</style>