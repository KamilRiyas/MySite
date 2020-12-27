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
    activeContent = eval(value);
  });
 
</script>

<profession>
    <SubNavBar {holder}/>
    <svelte:component this={activeContent} />
</profession>

<style>

</style>