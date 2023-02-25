<script lang="ts">
  	import AnnoucesMina from "$lib/AnnoucesMina.svelte";
	import Footer from "$lib/Footer.svelte";
	import Header from "$lib/Header.svelte";
	import HeroSearch from "$lib/HeroSearch.svelte";
  	import Options from "$lib/Options.svelte";
  	import Pagination from "$lib/Pagination.svelte";

	const websiteName = "Github";
	let searchHero: string = "";
	let checked: boolean = false;
	let option: string = "New York";
	let searchOption: string = "";

	function search() {
		console.log(`Search hero clicked value: '${searchHero}'`);
	}

	function onchange() {
		console.log(`
			OPTION: ${option},
			CHECKED: ${checked},
			VALUE: '${searchOption}'
		`);
	}
</script>

<svelte:head>
	<title>{websiteName} Jobs</title>
</svelte:head>

<main>
	<Header name={websiteName}/>
	<HeroSearch bind:value={searchHero} fn={search}/>
	<Options bind:checked={checked} bind:option={option} onchange={onchange} bind:value={searchOption}/>
	<AnnoucesMina />
	<Pagination />
	<Footer />
</main>

<style>
	main {
		max-width: 1212px;
		margin: 0 auto;
	}
</style>
