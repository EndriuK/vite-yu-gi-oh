<script>
import { store } from '../store.js';

export default {
    data(){
        return{
            store,
            
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-20">
                <select @change="$emit('filter_cards')" v-model="store.archetype_search">
                    <option value="">Seleziona Archetipo</option>
                    <option :value="archetype.archetype_name" v-for="archetype, index in store.archetypesList">{{ archetype.archetype_name}}</option>
                </select>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    select {
        margin-left: 10px;
        background-color: #fff;
        color: #000;
        border: 1px solid black;
        border-radius: none;
        padding: 10px 20px;
    }
</style>