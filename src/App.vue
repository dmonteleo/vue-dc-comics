<template>
  <div id="app">
    <Header :utente="mioUtente" :saluto="mioSaluto" />
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Main from './components/Main.vue'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  data() {
    return{
      mioSaluto: 'ciao ciao bambina',
      mioUtente: 'Giuseppe Verdi', 
      user: {
        name: 'Ugo', 
        lastname: 'De Ughi', 
        age: 30
      }
    }
  },
    components: { 
      Header: Header,
      Footer: Footer, 
      Main: Main
    }
}
</script>

<style lang="scss">

  // GENERAL 
  @import './assets/style/_general.scss';

  // VARS
  @import './assets/style/_vars.scss';

  // UTILS
  @import './assets/style/_utils.scss';


</style>
