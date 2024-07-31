<script>
import { store } from '../store.js'

export default {
    data() {
        return {
            store
        }
    }
}
</script>
<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-12 col-md-4" v-for="character in store.CharactersList" :key="character.id">
                {{ character.name }}
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    
</style>


