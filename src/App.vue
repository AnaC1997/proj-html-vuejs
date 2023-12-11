<script>
import PageHeader from "./components/PageHeader.vue"
import PageMain from "./components/PageMain.vue";
import pageFooter from "./components/PageFooter.vue"

//import axios from 'axios'; //importo Axios in caso di bisogno
import { store } from "./store.js"

export default {
	components: {
    PageHeader,
    PageMain,
    pageFooter
		
	},
	data() {
		return {
			store
		}
	},
	mounted() {

	},
	methods: {
		
	}
}
</script>

<template>
	<PageHeader/>
  <PageMain/>
  <pageFooter/>
</template>


<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped
@use './styles/general.scss';
</style>

<style scoped lang="scss">
// importo variabili
@use './styles/partials/variables' as *;

// ...qui eventuale SCSS di App.vue
</style>