<script>
import { store } from "../store.js"

export default {
    name: "PageHeader",
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
    <div>
        <h1>Sono un componente header</h1>
    </div>
</template>

<style scoped lang="scss">
// importo variabili
@use '../styles/partials/variables' as *;

// ...qui eventuale SCSS 
</style>