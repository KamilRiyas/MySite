<script>
	import { activeNav } from './stores/navigationStore';
	import Header from './components/HeaderComponents/Header.svelte';
	import Profession from './components/ContentComponents/Profession.svelte';
	import Passion from './components/ContentComponents/Passion.svelte';
	import Interest from './components/ContentComponents/Interest.svelte';

	let currentNav;

	const unsubscribe = activeNav.subscribe(value => {
		switch (value) {
			case 'Profession':
				currentNav = Profession;
				break;
			case 'Passion':
				currentNav = Passion;
				break;
			case 'Interest':
				currentNav = Interest;
				break;
			default:
				break;
		}
	});
</script>

<Header />
<main>
	<div class="main-content">
		<svelte:component this={currentNav} />
	</div>
</main>

<style>
	.main-content{

	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>