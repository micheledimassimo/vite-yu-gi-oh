<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

import axios from 'axios';
import { store } from './store.js';


export default {
  data() {
    return { 
      store
      
    }
  },
  

  components: {
    AppHeader,
    AppMain
  },
  created() {
    axios
      .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then((res) => {
        console.log('OGGETTO CREATO DA AXIOS:', res);
        console.log('DATI CHE CI HA RISPOSTO IL SERVER:', res.data);
        console.log('TUTTI I PERSONAGGI:', res.data.data);

        this.store.allCards = res.data.data;
      });
    }
  
  }

</script>

<template>
  <div>
   
    <AppHeader />
    
    <AppMain />
    
  </div>
</template>

<style lang="scss">
@use 'assets/scss/main' as *;
// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";
</style>
