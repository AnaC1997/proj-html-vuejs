<script>
import { store } from "../store.js"

export default {
    name: "AppServices",
    props: ["infoServices"],
    data() {
        return {
            store
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/svgs/${img}`, import.meta.url).href;
        }


    },
    mounted() {

    }
}
</script>

<template>
    <div class="styleContenuto padding1">
        <div class="container styleContenuto padding1">
            <h1 >Excellence in <span class="colorTitulo"> Services</span> </h1>
            <p>We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of
                experienced and renowned professionals. These are some options that you can hire.</p>
            <div class="d-flex wrapper">
                <div  v-for="info in infoServices" class="card widthCard">
                <span class="padding1 containerImg">
                    <img :src="getImagePath(info.img)" alt="">
                    <i class="fas fa-arrow-right"></i>
                </span>
            
                <h1 class="padding1">{{ info.title }}</h1>
                <p class="padding1">{{ info.paragrafo }}</p>

            </div>

            </div>
                
        </div>
    </div>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

.styleContenuto {
    background-color: #E2E3E7;
    

    h1 {
        font-size: 3rem;
        font-weight: bolder;
    }

    p {
        color: #828D94;
    }

    .wrapper{
      gap: 1rem;
      flex-wrap: wrap;
      justify-content: space-between;
    }

    .colorTitulo {
        color: #058283;
        background-color: #D3E2E4;
    }

    .widthCard {
        width: 30%;
        
    }

    img {
        width: 10%;
        color: #058283;

    }
    .containerImg{
        display: flex;
        justify-content: space-between;
        
    }

    .padding1{
        padding: 1rem;
    }

}
</style>