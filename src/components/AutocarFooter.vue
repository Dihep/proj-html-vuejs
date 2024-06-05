<script>
import store from '../data/store.js'

export default {
    components: {

    },

    data() {
        return {
            store
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
    <div id="footerWrapper">
        <div id="footerContent" class="w-75 mx-auto d-flex align-items-center">
            FOOTER
        </div>
    </div>
</template>

<style scoped>
    #footerWrapper {
        background-color: black;
        color: white;
    }
    #footerContent {
        font-size: 5rem;
    }

</style>
