<script>
import PageHeader from "./components/PageHeader.vue"
import PageMain from "./components/PageMain.vue"
import PageFooter from "./components/PageFooter.vue"
import AppSlider from "./components/AppSlider.vue"

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
						title: "Portafolio",
						items: ["About us", "Services", "Single service"],
					},
					{
						title: "Blog",
						items: ["About us", "Services", "Single service"],
					},
					{
						title: "Shop",
					}
				],
			},
			infoFooter:[
				{
                  title: "Company",
				  items:["Institutional", "Social & Events", "Innovation", "Environment", "Technology"]
				},
				{
                  title: "Services",
				  items:["Audit & Assurance", "Financial Advisory", "Innovation", "Environment", "Technology"]
				},
				{
                  title: "Consultants",
				  items:["David Cooper", "Oliver Jones", "Innovation", "Environment", "Technology"]
				}

			]




		}
	},
	mounted() {

	},
	methods: {


	}
}
</script>

<template>
	<!--Header-->
	<header>
		<PageHeader :info="infoHeader" />
	</header>

	<!--Main-->
	<main>
		<AppSlider />
		<PageMain />
	</main>

	<!--Footer-->
	<footer>
		<PageFooter  v-for=" info in store.infoContatti " :infoContact= "info" :infoItems="infoFooter"/>
	</footer>
</template>


<style lang="scss">
// importo il foglio di stile generale dell'applicazione, non-scoped
@use './styles/general.scss';
</style>

<style scoped lang="scss">
// importo variabili
@use './styles/partials/variables' as *;


</style>