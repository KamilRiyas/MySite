<script>
	import { activeNav,activeSubNav } from '../../stores/navigationStore.js';
	import SubNavBar from './SubNavBar.svelte';
	import Expertise from './Expertise.svelte';
	import Experience from './Experience.svelte';
	import Projects from './Projects.svelte';

	let holder;
	let activeContent = 'Expertise';

	const unsubscribeNav = activeNav.subscribe(value => {
		holder = value;
	});

	const unsubscribeContent = activeSubNav.subscribe(value => {
		switch (value) {
			case 'Expertise':
				activeContent = Expertise;
				break;
			case 'Experience':
				activeContent = Experience;
				break;
			case 'Projects':
				activeContent = Projects;
				break;
			default:
				break;
		}
	});
</script>

<profession>
    <SubNavBar {holder}/>
    <svelte:component this={activeContent} />
</profession>

<style>

</style>