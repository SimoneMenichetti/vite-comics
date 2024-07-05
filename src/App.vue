<script >
import AppHeader from './components/AppHeader.vue'

export default{
  name:'App',
  components:{
    AppHeader,
  }
}
</script>

<template>
  <AppHeader/>
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
