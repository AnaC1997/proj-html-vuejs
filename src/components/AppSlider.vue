<script>
import { store } from "../store.js"

export default {
    name: "AppSlider",
    data() {
        return {
            store,
            attualeSlider: 0,
            numSlides: 3
        }
    },
    methods: {
        back() {
            if (this.attualeSlider > 0) {
                this.attualeSlider--;
            }
            else {
                this.attualeSlider = this.numSlides -1;
            }

        },

        next() {

            if (this.attualeSlider < this.numSlides -1) {
                this.attualeSlider++;
            }
            else {
                this.attualeSlider = 0;
            }
        }

    },
    mounted() {

    }
}
</script>

<template>
    <section>
        <i @click="back()" class="fas fa-chevron-left"></i>
        <div v-show="attualeSlider === attualeSlider">
            <!--Idee-->
            <div class="container" v-if="attualeSlider === 0">
                <span class="contenutoTesto" >
                    <h1 class="share">WE Share </h1>
                    <h1 class="ideas">Good Ideas</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis, accusantium quidem
                        eligendi officia hic, possimus error vel, in molestias iure sunt dolore aliquam eaque esse fuga!
                        Doloribus,
                        soluta.</p>
                    <button class="btn">GET IN TOUCH</button>
                </span>
                <img src="../assets/img/woman.png" alt="">
            </div>
            <!--Team-->

            <div class="container" v-else-if="attualeSlider === 1">
                <img src="../assets/img/woman.png" alt="">
                <span class="contenutoTesto">
                    <h1 class="share">WE Share </h1>
                    <h1 class="ideas">Good Ideas</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis, accusantium quidem
                        eligendi officia hic, possimus error vel, in molestias iure sunt dolore aliquam eaque esse fuga!
                        Doloribus,
                        soluta.</p>
                    <button class="btn">GET IN TOUCH</button>
                </span>
                <img src="../assets/img/men.png" alt="">
            </div>

            <!--Consult-->
            <div class="container" v-else-if="attualeSlider === 2">
                <img src="../assets/img/men.png" alt="">
                <span class="contenutoTesto">
                    <h1 class="share">WE Share </h1>
                    <h1 class="ideas">Good Ideas</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis, accusantium quidem
                        eligendi officia hic, possimus error vel, in molestias iure sunt dolore aliquam eaque esse fuga!
                        Doloribus,
                        soluta.</p>
                    <button class="btn">GET IN TOUCH</button>
                </span>
            </div>
        </div>
        <i @click="next()" class="fas fa-chevron-right"></i>
    </section>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

section{
    display: flex;
    align-items: center;
    justify-content: center;


    .container {
    display: flex;
    height: 80vh;
    width: 100%;
    align-items: center;
    justify-content: center;
    

    img {
        width: 40%;
        height: 500px;
     
    }

    .contenutoTesto {
        width: 40%;
    }

    h1 {
        font-size: 3rem;
        font-weight: bold;
    }

    .ideas {
        color: #058283;

    }

    button {
        background-color: #058283;
        color: white;
    }



}

}


// ...qui eventuale SCSS </style>