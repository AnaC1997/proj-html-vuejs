<script>
import { store } from "../store.js"

export default {
    name: "AppCompany",
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
    <div class="styleContainer d-flex">
        <!--Informazione-->
        <div class="styleInformazione">
            <h1 class="p-3">The <span class="colorTitulo">Company</span></h1>
            <p>For 12 years we have been providing audit and warranty, financial advice, risk advice, taxes and related
                services to select clients.</p>

            <div class="d-flex">
                <span class="styleContent">
                    <span class="d-flex gap">
                        <i class="fas fa-hourglass"></i>
                        <h2>Tradition</h2>
                    </span>
                    <p>Lorem ipsum dolor sit amet consent elit</p>
                </span>
                <span class="styleContent">
                    <span class="d-flex gap">
                        <i class="fas fa-lock"></i>
                        <h2>Security</h2>
                    </span>
                    <p>Lorem ipsum dolor sit amet consent elit</p>

                </span>
            </div>

            <div class="d-flex">
                <span class="styleContent">
                    <span class="d-flex gap">
                        <i class="fab fa-apple"></i>
                        <h2>Certificate</h2>
                    </span>
                    <p>Lorem ipsum dolor sit amet consent elit</p>
                </span>
                <span class="styleContent">
                    <span class="d-flex gap">
                        <i class="fas fa-user"></i>
                        <h2>Expertise</h2>
                    </span>
                    <p>Lorem ipsum dolor sit amet consent elit</p>
                </span>
            </div>
        </div>

        <!--img-->
        <div class="styleImg">
            <img src="../assets/img/about-4.jpg" alt="">
        </div>
    </div>

</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;


.styleContainer {
    background-color: #132E43;
    display: flex;
    align-items: center;

    .styleContent {
        width: 40%;

    }

    h1 {
        font-weight: bolder;
        font-size: 3rem;
    }
    .colorTitulo {
        color: #058283;
        background-color: #D3E2E4;
       
    }

    h2 {
        font-weight: bold;
        font-size: 2rem;

    }

    .fab {
        color: #08A2A4;
        font-size: 2rem;
    }

    .fas {
        color: #08A2A4;
        font-size: 2rem;
    }

    .gap {
        gap: 1rem;
    }

    .styleInformazione {
        width: 50%;
        padding-left: 6rem;
        color: white;
    }

    p {
        color: #9099A0;
        padding-bottom: 2rem;
    }

}

.styleImg {
    width: 50%;

    img {
        width: 100%;
    }
}
</style>