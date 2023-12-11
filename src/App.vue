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
			store,
			infoHeader: [
				{
					img: "svg-7.svg",
				},
				{
					opzione1: "Demos",
					homeOptions: [
						"Home 1",
						"Home 2",
						"Home 3",
						"Home 4",
						"Home 5",
						"Home 6",
						"Home 7",
						"Home 8",
						"Home 9",
						"Home 10",
						"Home 11",
					],
				},
				{
					opzione2: "Pages",
					pagesOptions: ["About us", "Services", "Single service"],
				},
				{
					opzione3:"Portafolio",
					portafoloOptions: ["About us", "Services", "Single service"],
				},
				{
					opzione4:"Blog",
					blogOptions: ["About us", "Services", "Single service"],
				},
				{
					opzione4:"Shop",
				}
			],
		
		}
	},
	mounted() {

	},
	methods: {

	}
}
</script>

<template>
	<PageHeader :info="infoHeader"/>
	<PageMain />
	<pageFooter />
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