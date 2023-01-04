<script>
	//@ts-ignore
	import Header from "./Header.svelte";
	import AboutMe from "./AboutMe.svelte";
	import Projetos from "./Projetos.svelte";
	import Achievements from "./Achievements.svelte";
	import Footer from "./Footer.svelte";
</script>

<div class="main">
	<Header />

	<AboutMe />

	<Projetos />

	<Achievements />
</div>

<Footer />

<style>
	* {
		font-family: "Open Sans", sans-serif;
	}

	div.main {
		display: flex !important;
		flex-direction: column;
		gap: 10vh;
	}

	@media screen and (max-width: 990px) {
		div.main {
			gap: 5vh;
		}
	}
</style>
