<script lang="ts">
  import AnounceMina from "$lib/AnounceMina.svelte";
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
  <Header name={websiteName} />
  <HeroSearch bind:value={searchHero} fn={search} />
  <div class="content">
    <span>
      <Options bind:checked bind:option {onchange} bind:value={searchOption} />
    </span>
    <span>
      <AnounceMina
        img="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8cG9ydHJhaXR8ZW58MHx8MHx8&w=1000&q=80"
        company="Google"
        title="Titre annonce"
        day={1}
        city="New York"
        fulltime
      />
      <AnounceMina
        img="https://www.naturepaysage.photo/wp-content/uploads/Nature-Paysage-portfolio-17-novembre-2019-0017-3.jpg"
        company="Apple"
        title="Titre annonce"
        day={10}
        city="Los angeles"
      />
      <AnounceMina
        img=""
        company="Apple"
        title="Titre annonce"
        day={10}
        city="Los angeles"
      />
      <AnounceMina
        img="https://www.naturepaysage.photo/wp-content/uploads/Nature-Paysage-portfolio-17-novembre-2019-0017-3.jpg"
        company="Apple"
        title="Titre annonce"
        day={10}
        city="Los angeles"
        fulltime
      />
      <AnounceMina
        img=""
        company="Apple"
        title="Titre annonce"
        day={10}
        city="Los angeles"
      />
      <Pagination />
    </span>
  </div>
  <Footer />
</main>

<style>
  main {
    max-width: 1212px;
    margin: 0 auto;
  }

  .content {
	display: flex;
	max-width: 1200px;
	gap: 32px;
	margin: 0 12px;
  }

  .content span:nth-child(2) {
	width: 100%;
  }

  @media screen and (max-width: 768px) {
	.content {
		flex-direction: column;
	}
  }
</style>
