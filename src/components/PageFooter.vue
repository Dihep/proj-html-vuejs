<script>
import AutocarFooter from './AutocarFooter.vue'
import store from `../data/store.vue`

export default {
    components: {
        AutocarFooter
    },

    data() {
        return {
            store,

        }
    },

    methods: {
        getImg(path) {
            let risultato = new URL(`../assets/Img/${path}`, import.meta.url);
            return risultato.href;
        },
    }
}
</script>

<template>
    
</template>

<style scoped>

</style>
