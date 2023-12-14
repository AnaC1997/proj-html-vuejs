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
                    title: "Audit & Assurance",
                    paragrafo: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."

                },
                {
                    img: "svg-2.svg",
                    title: "Financial Advisory",
                    paragrafo: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."

                },
                {
                    img: "svg-3.svg",
                    title: "Analytics and M&A",
                    paragrafo: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."

                },
                {
                    img: "svg-4.svg",
                    title: "Middle Marketing",
                    paragrafo: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."

                },
                {
                    img: "svg-5.svg",
                    title: "Legal Consulting",
                    paragrafo: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."

                },
                {
                    img: "svg-6.svg",
                    title: "Regolatory Risk",
                    paragrafo: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa expedita reiciendis."

                }
            ],
            menuProjects: [
                {
                    items: ["ALL", "ENVIRONMENT", "EVENTS", "INSTITUTIONAL", "SOCIAL", "TECHNOLOGY", "INNOVATION"]


                }
            ],
            cardProjects: [
                {
                    img: "portfolio1.jpeg",
                    tipe: "Codings",
                    year: "3 year",
                    title: "Portafolio item with intro with sidebar",
                    paragrafo: "Lorem lorem lorem lorem lorem lorem lorem lorem"
                },
                {
                    img: "portfolio2.jpeg",
                    tipe: "Codings",
                    year: "3 year",
                    title: "Portafolio item with intro with sidebar",
                },
                {
                    img: "portfolio3.jpeg",
                    tipe: "Codings",
                    year: "3 year",
                    title: "Portafolio item with intro with sidebar",
                    paragrafo: "Lorem lorem lorem lorem lorem lorem lorem lorem"

                },
                {
                    img: "portfolio4.jpeg",
                    tipe: "Codings",
                    year: "3 year",
                    title: "Portafolio item with intro with sidebar",
                },
                {
                    img: "portfolio5.jpeg",
                    tipe: "Codings",
                    year: "3 year",
                    title: "Portafolio item with intro with sidebar",
                    paragrafo: "Lorem lorem lorem lorem lorem lorem lorem lorem"

                },
                {
                    img: "portfolio6.jpeg",
                    tipe: "Codings",
                    year: "3 year",
                    title: "Portafolio item with intro with sidebar",
                },

            ],
            infoCompNumber: [
                {
                    number: 128,
                    item: "Certifications",
                },
                {
                    number: 230,
                    item: "Employees",
                },
                {
                    number: 517,
                    item: "Customers",
                },
                {
                    number: 94,
                    item: "Countries Served",
                },

            ],
            imgNumbers:[
                {
                    img: "logo-1.png"
                },
                {
                    img: "logo-2.png"
                },
                {
                    img: "logo-3.png"
                },
                {
                    img: "logo-4.png"
                },
                {
                    img: "logo-5.png"
                }
            ]
            


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
        <AppServices :infoServices="contentServices" />
    </section>

    <!--Company-->
    <section>
        <AppCompany />
    </section>

    <!--Projects-->
    <section>
        <AppProyects :infoProyects="menuProjects" :cardsProps="cardProjects" />
    </section>

    <!--Numbers-->
    <section>
        <AppNumbers :infoNumbers="infoCompNumber" :imgNumbers="imgNumbers" />
    </section>

    <!--Touch-->
    <section>
        <AppTouch v-for=" info in store.infoContatti " :infoContact= "info" />
    </section>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;



</style>