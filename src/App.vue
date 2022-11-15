<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppIcons from './components/AppIcons.vue';
import AppFooter from './components/AppFooter.vue';
import AppFooterSocial from './components/AppFooterSocial.vue';

export default {
  name: 'App',

  components: {
    AppHeader,
    AppMain,
    AppIcons,
    AppFooter,
    AppFooterSocial
  }
}

</script>

<template>

  <AppHeader/>

  <AppMain/>

  <AppIcons/>

  <AppFooter/>

  <AppFooterSocial/>
  
</template>

<style lang="scss">

@use './style/general.scss'

</style>
