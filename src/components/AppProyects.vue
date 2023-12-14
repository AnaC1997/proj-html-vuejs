<script>
import { store } from "../store.js"

export default {
    name: "AppProyects",
    props: {
        infoProyects: Array,
        cardsProps: Array
    },
    data() {
        return {
            store
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }

    },
    mounted() {

    }
}
</script>

<template>
    <div class="container text-center styleContainer ">
        <h1>Actions & <span class="colorTitulo"> Proyects</span></h1>
        <div class="d-flex align-items-center justify-content-center" v-for="project in infoProyects" :key="project.id">
            <p class="p-3" v-for="item in project.items">{{ item }}</p>
        </div>

        <div class="containerCard d-flex">
            <div v-for="card in cardsProps" class="card text-bg-dark cardImg">
                <img :src="getImagePath(card.img)" class="card-img" alt="img">
                <div class="card-img-overlay d-flex flex-column justify-content-between">
                    <span class="d-flex justify-content-center">
                        <p class="p-2"><i class="fas fa-user"></i> {{ card.tipe }}</p>
                        <p class="p-2"> <i class="fas fa-clock"></i> {{ card.year }}</p>
                    </span>
                    <div>
                        <h5 class="card-title">{{ card.title }}</h5>
                        <p class="card-text colorParagrafo"><small>{{ card.paragrafo }}</small></p>
                    </div>

                </div>
            </div>

        </div>
    </div>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

.styleContainer{
    padding-top: 4rem;
    padding-bottom: 5rem;

}

h1 {
    font-weight: bolder;
    font-size: 2.5rem;
}

h5 {
    font-weight: bolder;
    font-size: 1.5rem;

}

.colorParagrafo {
    color: #abb7c0;

}

.colorTitulo {
    color: #058283;
    background-color: #D3E2E4;

}


.containerCard {
    flex-wrap: wrap;
    position: relative;



    .cardImg {
        color: white;
        width: 30%;
        height: 350px;
        border-style: none;
        margin: 1rem;

    }

    img {
        width: 100%;
        height: 100%;



    }


}
</style>