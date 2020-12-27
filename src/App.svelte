<script>
	import { activeNav } from './stores/navigationStore';
	import Header from './components/HeaderComponents/Header.svelte';
	import Profession from './components/ContentComponents/Profession.svelte';
	import Passion from './components/ContentComponents/Passion.svelte';
	import Interest from './components/ContentComponents/Interest.svelte';

	let currentNav;

	const unsubscribe = activeNav.subscribe(value => {
		currentNav = eval(value);
	});
</script>

<Header />
<main>
	<svelte:component this={currentNav} />
</main>

<style>
	main {

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