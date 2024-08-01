<!-- <script>
import { store } from './store.js';
import axios from 'axios';

import AppHeader from './components/AppHeader.vue';
import CharactersList from './components/CharactersList.vue';

export default {
  components: {
    AppHeader,
    CharactersList,
  },
  created() {
    this.getCharactersList()
  },
  methods: {
    getCharactersList(){
      axios.get(store.apiUrl).then((result) => {
        store.CharactersList = result.data.data
      });
    }
  },
  data() {
    return {
      store,
    }
  }
}
</script>
<template>
  <AppHeader />
  <main>
    <CharactersList />
  </main>
</template>
<style lang="scss">
@import "./components/syles/generals.scss"
</style>
 -->


 <script>
import AppHeader from './components/AppHeader.vue';
import CardsList from './components/CardsList.vue';

 export default {
  components: {
    AppHeader,
    CardsList,
  }
 }
 </script>
 <template lang="">
  <AppHeader />
  <main>
    <CardsList />
  </main>
 </template>
 <style lang="scss">
  @import './components/syles/generals.scss'
 </style>