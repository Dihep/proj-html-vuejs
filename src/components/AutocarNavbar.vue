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

    <nav>

        <div id="navContent" class="w-75 mx-auto d-flex align-items-center">
            <div id="navLogo">
                <img :src="getImg(store.navbarLogo)" alt="">
            </div>
            <ul>
                <li v-for="link in store.headerData.navbarLinks">  
                    {{ link }}
                </li>
            </ul>
            <div id="navMyAccount" class="navButton"> 
                <img src="../assets/Icone/padlock.png" alt="">
                My Account
            </div>
            <div id="navAddCar" class="navButton">
                <img src="../assets/Icone/add.png" alt="">
                Add Car
            </div>
            <!-- Offcanvas -->
            <div id="navPhoneNumber" class="navButton">
                <img src="../assets/Icone/padlock.png" alt="">
                {{store.headerData.navbarPhoneNumber}}
            </div>
        </div>

    </nav>

</template>

<style scoped>
nav {
    background-color: white;
}
#navContent {
    height: 5rem;
    gap: 0.2rem;
    justify-content: space-between;
}

#navLogo {
    width: 15%;
}
#navLogo img {
    height: 3rem;
}

.navButton {
    background-color: black;
    color: white;
    font-size: 0.8rem;
    max-height: 3rem;
    border-radius: 0.2rem;
    padding: 0.8rem 0;
}
.navButton img {
    height: 1.5rem;
    filter: invert(1);
}

li {
    display: inline-block;
    margin: 0 0.2rem;
    font-size: 0.8rem;
    color: black;
}
ul {
    list-style: none;
    padding: 0;
    margin: 0;
}
</style>
