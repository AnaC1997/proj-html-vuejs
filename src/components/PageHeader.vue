<script>
import { store } from "../store.js"

export default {
    name: "PageHeader",
    props: ["info"],
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
    <header class="container">
        <nav v-for="infoNav in info">
            <div>
                <a href="#">
                    <img :src="getImagePath(infoNav.img)" alt=""></a>
            </div>
            <div>
                <ul>{{ infoNav.opzione1 }}
                    <li v-for="option in infoNav.homeOptions"><a href="#">{{ option }}</a></li>
                </ul>

                <ul>{{ infoNav.opzione2 }}
                    <li v-for="option in infoNav.pagesOptions"><a href="#">{{ option }}</a></li>
                </ul>
                <ul>{{ infoNav.opzione3 }}
                    <li v-for="option in infoNav.portafoloOptions"><a href="#">{{ option }}</a></li>
                </ul>
                <ul>{{ infoNav.opzione4 }}
                    <li v-for="option in infoNav.blogOptions"><a href="#">{{ option }}</a></li>
                </ul>
            </div>
        </nav>

    </header>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

header {
    height: 700px;
    display: flex;

    img {
        width: 50%;
    }
    div{
        display: flex;
    }
}
</style>
