
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