<script>
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import CardsList from './components/CardsList.vue';

 export default {
  components: {
    AppHeader,
    CardsList,
  },
  created() {

  },
  methods: {
    showText() {
      alert(store.searchText);
    }
  },
 }
 </script>
 <template lang="">
  <AppHeader @search="showText()" />
  <main>
    <CardsList />
  </main>
 </template>
 <style lang="scss">
  @import './components/syles/generals.scss'
 </style>