<script>
import { store } from "../store.js"

export default {
    name: "AppNumbers",
    props: ["infoNumbers", "imgNumbers"],
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
    <div class="styleContainer  d-flex  align-items-center ">
        <div class="container text-center">
            <span>
                <h1 class="styleNumber p-1">Results in Numbers</h1>
                <p class="p-2 colorTesto">Our goal is to exceed expectations by delivering the best job possible.</p>
            </span>
            <div class="d-flex justify-content-around p-3">
                <span v-for="infoNumber in infoNumbers">
                    <h1 class="styleNumber colorNumber p-1">{{ infoNumber.number }}</h1>
                    <p class="colorTesto">{{ infoNumber.item }}</p>
                </span>
            </div>
        </div>
    </div>
    <img class="imgPositAbsoluto" src="../assets/svgs/svg-0.svg" alt="">
    <div class="styleLog d-flex  justify-content-around">
        <img class="styleImagLg" v-for="info in imgNumbers" :src="getImagePath(info.img)" alt="">
    </div>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

.styleContainer {
    background-image: url(../assets/img/bg-7.jpg);
    opacity: 0.9;
    color: white;
    height: 550px;
    width: 100%;
    position: relative;



    .colorNumber {
        color: #09A4A6;
    }

    .colorTesto {
        color: #828D94;

    }

    .styleNumber {
        font-weight: bold;
        font-size: 3rem;

    }
}

.imgPositAbsoluto {
    position: absolute;
    left: 50%;
    top: 528%;
    transform: translate(-50%, -50%);

}

.styleLog {
    background-color: #102636;
    background: linear-gradient(to right, #0D1B2A, #102537, #183E57, #1C4966);
    color: red;
    padding: 4rem;



}

.styleImagLg {
    filter: brightness(700%);

}
</style>