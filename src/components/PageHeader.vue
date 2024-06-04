<script>
import AutocarNavbar from './AutocarNavbar.vue'
import store from `../data/store.vue`

export default {
    components: {
        AutocarNavbar
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

<style scoped></style>
