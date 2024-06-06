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
            <div id="navButtons">
                <div id="navMyAccount" class="navButton">
                    <img src="../assets/Icone/padlock.png" alt="">
                    My Account
                </div>
                <div id="navAddCar" class="navButton">
                    <img src="../assets/Icone/add.png" alt="">
                    Add Car
                </div>
                <!-- Offcanvas -->
                <div id="offcanvas">
                    <i class="fa-solid fa-bars-staggered"></i>
                </div>
                <div id="navPhoneNumber" class="navButton">
                    <img src="../assets/Icone/headphones.png" alt="">
                    {{ store.footerData.autocarInfo.acPhone.text }}
                </div>
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
    gap: 0.3rem;
    justify-content: space-between;
    font-weight: 600;
}

#navLogo {
    width: 15%;
}

#navLogo img {
    height: 3rem;
}

#navButtons {
    display: flex;
    gap: 0.8rem;
}
.navButton {
    background-color: black;
    color: white;
    font-size: 1rem;
    border-radius: 0.2rem;
    padding: 0.6rem 0.5em;
}
.navButton img {
    height: 1.5rem;
    filter: invert(1);
    margin-right: 0.5rem;
}
ul {
    list-style: none;
    padding: 0;
    margin: 0;
}
li {
    display: inline-block;
    margin: 0 0.5rem;
    font-size: 1rem;
    color: black;
}

/* Stili offcanvas */
#offcanvas {
    height: 3rem;
    color: black;
    font-size: 2rem;
    padding: 0 0.6rem;
}
#offcanvas i {
    position: relative;
    bottom: 5%;
}
</style>
