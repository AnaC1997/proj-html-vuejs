<script>
import { store } from "../store.js"
import AppServices from "./AppServices.vue"
import AppCompany from "./AppCompany.vue"
import AppProyects from "./AppProyects.vue"
import AppNumbers from "./AppNumbers.vue"
import AppTouch from "./AppTouch.vue"


export default {
    name: "PageMain",
    components: {
        AppServices,
        AppCompany,
        AppProyects,
        AppNumbers,
        AppTouch,

    },
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
    <!--Services-->
    <section>
        <AppServices />
    </section>

    <!--Company-->
    <section>
        <AppCompany />
    </section>

    <!--Projects-->
    <section>
        <AppProyects />
    </section>

    <!--Numbers-->
    <section>
        <AppNumbers />
    </section>

    <!--Touch-->
    <section>
        <AppTouch />
    </section>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

// ...qui eventuale SCSS </style>