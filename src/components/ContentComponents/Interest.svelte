<script>
    import { activeNav,activeSubNav } from '../../stores/navigationStore.js';
    import SubNavBar from './SubNavBar.svelte';
    import Music from './Music.svelte';
    import Movies from './Movies.svelte';
    import Anime from './Anime.svelte';

    let holder;
    let activeContent;

    const unsubscribeNav = activeNav.subscribe(value => {
        holder = value;
    });

    const unsubscribeContent = activeSubNav.subscribe(value => {
        switch (value) {
			case 'Music':
				activeContent = Music;
				break;
			case 'Movies':
				activeContent = Movies;
				break;
			case 'Anime':
				activeContent = Anime;
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