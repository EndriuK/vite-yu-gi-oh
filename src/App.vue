<script>
import { store } from './store.js';
import axios from 'axios';

import AppHeader from './components/AppHeader.vue';
import CharacterList from './components/CharactersList.vue';

export default {
  components: {
    AppHeader,
    CharacterList,
  },
  created() {
    this.getCharactersList()
  },
  methods: {
    getCharactersList(){
      axios.get(store.apiUrl).then((result) => {
        store.CharacterList = result.data
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

