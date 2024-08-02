<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import CardsList from './components/CardsList.vue';
import FilterCards from './components/FilterCards.vue';


 export default {
  components: {
    AppHeader,
    CardsList,
    FilterCards
    
  },
  created() {
        this.getCards();
        this.getArchetypes();
  },
  methods: {
    getCards() {
      if(store.archetype_search !== ''){
        axios.get(`${store.apiUrl}&archetype=${store.archetype_search}`).then((response) => {
        store.cardsList = response.data.data;
        store.loading = false;
      });
      }
      else{
        axios.get(store.apiUrl).then((response) => {
          store.cardsList = response.data.data;
          store.loading = false;
        });
      }
    }, 
    getArchetypes() {
      axios.get(store.apiArchetypesUrl).then((response) => {
        for(let i=0; i<10; i++) {
          store.archetypesList.push(response.data[i]);
        }
      });
    }
  },
 }
 </script>
 <template lang="">
  <AppHeader  />
  <main>
    <FilterCards @filter_cards="getCards()" />
    <CardsList />
  </main>
 </template>
 <style lang="scss">
  @import './components/syles/generals.scss'
 </style>