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
        activeContent = eval(value);
    });
 
</script>

<profession>
    <SubNavBar {holder}/>
    <svelte:component this={activeContent} />
</profession>

<style>

</style>