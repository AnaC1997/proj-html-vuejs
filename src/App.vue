<script>
import PageHeader from "./components/PageHeader.vue"
import PageMain from "./components/PageMain.vue"
import PageFooter from "./components/PageFooter.vue"
import AppSlider from"./components/AppSlider.vue"

//import axios from 'axios'; //importo Axios in caso di bisogno
import { store } from "./store.js"

export default {
	components: {
		PageHeader,
		PageMain,
		PageFooter,
		AppSlider

	},
	data() {
		return {
			store,
			infoHeader: 
				{
					img: "svg-7.svg",
					options: [
					{
					title: "Demos",
					items: [
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
					title: "Pages",
					items: ["About us", "Services", "Single service"],
				},
				{
					title:"Portafolio",
					items: ["About us", "Services", "Single service"],
				},
				{
					title:"Blog",
					items: ["About us", "Services", "Single service"],
				},
				{
					items:"Shop",
				}
			],
				},
				
				
		
		}
	},
	mounted() {

	},
	methods: {

	}
}
</script>

<template>
	<header>
		<PageHeader :info="infoHeader" />
	</header>
	<main>
		
	<AppSlider/>
	<PageMain />

	</main>
	
	<PageFooter />
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