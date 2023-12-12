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
            store,
            contentServices: [
                {
                    img: "svg-1.svg",
                    title:"Audit & Assurance",
                    paragrafo:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."
                     
                },
                {
                    img: "svg-2.svg",
                    title:"Financial Advisory",
                    paragrafo:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."
                     
                },
                {
                    img: "svg-3.svg",
                    title:"Analytics and M&A",
                    paragrafo:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."
                     
                },
                {
                    img: "svg-4.svg",
                    title:"Middle Marketing",
                    paragrafo:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."
                     
                },
                {
                    img: "svg-5.svg",
                    title:"Legal Consulting",
                    paragrafo:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."
                     
                },
                {
                    img: "svg-6.svg",
                    title:"Regolatory Risk",
                    paragrafo:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."
                     
                }
            ],

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
    <section >
        <AppServices :infoServices="contentServices" />
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