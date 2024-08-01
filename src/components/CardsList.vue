<script>
import axios from 'axios';
import { store } from '../store.js';
import DetailCard from './DetailCard.vue';

export default {
    components: {
        DetailCard
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
            });
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <DetailCard v-for="card in store.cardsList" :key="card.id" :card="card"/>
        </div>
        
    </div>
</template>
<style lang="scss" scoped>
    
</style>