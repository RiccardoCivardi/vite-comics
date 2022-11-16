<script>

import AppHeader from './components/AppHeader.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppMain from './components/AppMain.vue';
import AppIcons from './components/AppIcons.vue';
import AppFooter from './components/AppFooter.vue';

export default {

  name: 'App',

  components: {
    AppHeader,
    AppJumbo,
    AppMain,
    AppIcons,
    AppFooter
  }

}

</script>

<template>

  <AppHeader/>

  <AppJumbo/>

  <AppMain/>

  <AppIcons/>

  <AppFooter/>
  
</template>

<style lang="scss">

@use './style/general.scss';

</style>
