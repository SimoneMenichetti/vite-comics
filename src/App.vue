<script >
// Importazione dei componenti da utilizzare nell'applicazione
import AppHeader from './components/layout/AppHeader.vue'
import AppJumbotron from './components/layout/AppJumbotron.vue';
import AppMain from './components/AppMain.vue'
import AppFeatures from './components/common/AppFeatures.vue';
import AppFooter from './components/layout/AppFooter.vue';


export default{
  // Registrazione dei componenti figli per essere utilizzati nel template
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
    <!-- Struttura del layout principale dell'applicazione -->
  <AppHeader/>
  <AppJumbotron/>
  <AppMain/>
  <AppFeatures/>
  <AppFooter/>
  
</template>


<style lang="scss">
 // Importazione di variabili e stili generali usando SCSS
  @use './assets/styles/variables' as*;
  @use './assets/styles/general.scss' as*;

  // Stile per gli elementi di intestazione (h1-h6)

  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {

    color: $primary;

  }
</style>
