<script >
import AppHeader from './components/AppHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue'
import AppFeatures from './components/AppFeatures.vue';
import AppFooter from './components/AppFooter.vue'





export default{
  name:'App',
  components:{
    AppHeader,
    AppJumbotron,
    AppMain,
    AppFeatures,
    AppFooter,
   
  }
}
</script>

<template>
  <AppHeader/>
  <AppJumbotron/>
  <AppMain/>
  <AppFeatures/>
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
