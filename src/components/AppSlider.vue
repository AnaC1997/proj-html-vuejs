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
                this.attualeSlider = this.numSlides - 1;
            }

        },

        next() {

            if (this.attualeSlider < this.numSlides - 1) {
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
        <i @click="back()" class="fas fa-chevron-left" style="color: #058283;"></i>
        <div v-show="attualeSlider === attualeSlider">
            <!--Idee-->
            <div class="container containerStyle" v-if="attualeSlider === 0">
                <span class="contenutoTesto">
                    <h1>We Share <span class="colorTitulo"> Good Ideas</span> </h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis, accusantium quidem
                        eligendi officia hic, possimus error vel, in molestias iure sunt dolore aliquam eaque esse fuga!
                        Doloribus,
                        soluta.</p>
                    <button class="btn">GET IN TOUCH</button>
                </span>
                <img src="../assets/img/bgDonna.png" alt="">
            </div>
            <!--Team-->

            <div class="container containerStyle" v-else-if="attualeSlider === 1">
                <img src="../assets/img/bgDonna.png" alt="">
                <span class="contenutoTesto">
                    <h1>We Share <span class="colorTitulo"> Good Ideas</span> </h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis, accusantium quidem
                        eligendi officia hic, possimus error vel, in molestias iure sunt dolore aliquam eaque esse fuga!
                        Doloribus,
                        soluta.</p>
                    <button class="btn">GET IN TOUCH</button>
                </span>
                <img src="../assets/img/bgUomo.png" alt="">
            </div>

            <!--Consult-->
            <div class="container containerStyle" v-else-if="attualeSlider === 2">
                <img src="../assets/img/bgUomo.png" alt="">
                <span class="contenutoTesto">
                    <h1>We Share <span class="colorTitulo"> Good Ideas</span> </h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis, accusantium quidem
                        eligendi officia hic, possimus error vel, in molestias iure sunt dolore aliquam eaque esse fuga!
                        Doloribus,
                        soluta.</p>
                    <button class="btn">GET IN TOUCH</button>
                </span>
            </div>
        </div>
        <i @click="next()" class="fas fa-chevron-right" style="color: #058283;"></i>
    </section>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

section {
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.3s ease, color 0.3s ease;

    &:hover {
            background-color: #D3E2E4; 
            color: #058283;
        }

    .containerStyle {
        display: flex;
        height: 90vh;
        width: 100%;
        align-items: center;
        justify-content: center;
        

        p {
            color: #828D94;
            transition: color 0.3s ease;
        }

        p:hover{
           color: #95b2c6;
        }

        img {
            width: 35%;
            height: 90vh;
           
        }

        .contenutoTesto {
            width: 60%;
           
        }

        h1 {
            font-size: 3rem;
            font-weight: bolder;
        }

        .colorTitulo {
            color: #058283;
            background-color: #D3E2E4;
            transition: color 0.3s ease, background-color 0.3s ease;
        }

        button {
            background-color: #058283;
            color: white;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        button:hover{
          background-color:  #779fba;
          padding: 1rem;
        }
    }
}


</style>