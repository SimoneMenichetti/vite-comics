<script >
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'

export default{
  name:'App',
  components:{
    AppHeader,
    AppFooter,
  }
}
</script>

<template>
  <AppHeader/>
  <AppFooter/>
</template>

<style lang="scss">
  @use './assets/styles/variables' as*;
  @use './assets/styles/general.scss' as*;

  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {

    color: $primary;

  }
</style>
