<script>
import { store } from "../store.js"

export default {
    name: "PageFooter",
    props: ["infoContact", "infoItems"],
    data() {
        return {
            store
        }
    },
    methods: {

    },
    mounted() {

    }
}
</script>

<template>
    <div class="styleContainer ">
        <div class="container d-flex pb-4">
            <!--column1-->
            <div class="grey columnlog ">
                <span class="p-1">
                    <img src="../assets/svgs/svg-7.svg" alt="">
                </span>
                <p class="p-2">Built to the smallest detail with
                    a focus on feature availability.</p>
                <p><i class="fas fa-phone"></i> {{ infoContact.telefono }}</p>
                <p><i class="fas fa-envelope"></i> {{ infoContact.mail }}</p>
                <p><i class="fas fa-map-marker"></i> {{ infoContact.indirizzo1 }}</p>
                <button class="btn btn-primary">BUY NEXGEN</button>
            </div>

            <div class="column" v-for="infoItem in infoItems">
                <ul class="card">
                    <h3 class="white">{{ infoItem.title }}</h3>
                    <li class="list-group-item" v-for="item in infoItem.items"><a class="nav-link grey" href="">{{ item
                    }}</a></li>
                </ul>
            </div>
        </div>
        <div class="darkBlue p-4 mt-4">
            <div class="container d-flex justify-content-between">
                <div class="">
                    <p class="grey">© 2023 - All rights reserved. Nexgen is maintained by Codings Group.</p>
                </div>

                <div class="grey px-1">
                    <i class="fab fa-facebook p-2"></i>
                    <i class="fab fa-instagram p-2"></i>
                    <i class="fab fa-telegram p-2"></i>
                </div>
            </div>
        </div>


    </div>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

.styleContainer {
    background-color: #143146;
    padding-top: 4rem;
   

    .columnlog {
        width: 40%;

    }

    img {
        width: 50%;

    }

    .grey {
        color: #828D94;
    }

    .column {
        width: 40%;
    }

    .card {
        padding: 2rem;
        margin: 1rem;
        background-color: #1C3D53;
    }

    .white {
        color: rgb(254, 254, 255);

    }

    .darkBlue {
        background-color: #1C2531;

    }
}</style>