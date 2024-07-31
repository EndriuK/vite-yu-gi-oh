<script>
import { store } from './store.js';
import axios from 'axios';

export default {
  components: {

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
  <div class="container">
      <div class="row">

      </div>
  </div>
</template>
<style lang="scss">
  
</style>