<script>
import { store } from './store.js';
import axios from 'axios';

import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    AppHeader
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
  <div class="container">
      <div class="row">
        
      </div>
  </div>
</template>
<style lang="scss">
  @import './styles/generals.scss'
</style>