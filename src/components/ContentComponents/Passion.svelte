<script>
    import { activeNav,activeSubNav } from '../../stores/navigationStore.js';
    import SubNavBar from './SubNavBar.svelte';
    import Hiking from './Hiking.svelte';
    import Photography from './Photography.svelte';
    import Badminton from './Badminton.svelte';
    
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