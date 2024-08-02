<script>
import axios from 'axios';
import { store } from '../store.js';
import DetailCard from './DetailCard.vue';
import AppLoader from './AppLoader.vue';
import FilterCards from './FilterCards.vue';

export default {
    components: {
        DetailCard,
        AppLoader,
        FilterCards
    },
    data() {
        return{
            store,
        }
    },
    created() {
        this.getCards()
    },
    methods: {
        getCards() {
            axios.get(store.apiUrl).then((response) => {
                store.cardsList = response.data.data;
                store.loading = false;
            });
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <AppLoader v-if="store.loading" />
        <div class="row" v-else>
            <DetailCard v-for="card in store.cardsList" :key="card.id" :card="card"/>
        </div>
        
    </div>
</template>
<style lang="scss" scoped>
    
</style>