<script>
	import Header from './components/Header.svelte';
</script>

<Header/>
<main>
	<h1>Hello World!🤗</h1>
	<p>Site is currently under construction.🙄</p>
	<p>Being built using Svelte</p>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>