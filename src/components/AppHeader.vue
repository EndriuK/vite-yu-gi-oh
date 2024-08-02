<!-- <script>
export default {
    
}
</script>
<template lang="">
    <header>
        <h1>Yu-Gi-Oh Api</h1>
    </header>
</template>
<style lang="scss">
    header {
        background-color: #fff;
        color: #000;
        padding: 30px 15px;
    }
</style> -->

<script>
import { store } from '../store.js'
export default {
    data() {
        return {
            store
        }
    },
}
</script>
<template lang="">
    <header class="my-2">
        <div class="container">
            <div class="row">
                <div class="col-6">
                    <h1>Yu-Gi-Oh Api</h1>
                </div>
                <!-- <div class="col-6">
                    <input type="text" class="form-control mt-3" placeholder="Search" v-model="store.searchText" @keyup.enter="$emit('search')">
                </div> -->
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    header {
        background-color: #fff;
        color: #000;
        padding: 30px 15px;
    }
</style>