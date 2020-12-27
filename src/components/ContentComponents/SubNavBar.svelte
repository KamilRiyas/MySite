<script>
    import { activeSubNav } from '../../stores/navigationStore.js';
    export let holder = '';

    let navs = [];
    let professionNavs = ['Expertise','Experience','Projects'];
    let passionNavs = ['Hiking','Photography','Badminton'];
    let interestNavs = ['Music','Movies','Anime'];
    let activeMenu;

    switch (holder) {
        case 'Profession':
            navs = professionNavs;
            break;
        case 'Passion':
            navs = passionNavs;
            break;
        case 'Interest':
            navs = interestNavs;
            break;
        default:
            break;
    }

    const unsubscribeContent = activeSubNav.subscribe(value => {
        activeMenu = value;
    });

    const handleClick = (e) => {
        //update the store about the active menu
        activeSubNav.update(value => e.srcElement.innerText);
        //update the UI to show the active menu
        activeMenu = e.srcElement.innerText;
        //update store value with the nav object
    }

</script>

<subNavBar>
    <ul>
        {#each navs as nav}
            <li on:click={e => handleClick(e)} class:active={nav === activeMenu}>{nav}</li>
        {/each}
    </ul>
</subNavBar>

<style>
    ul{
        list-style-type: none;
        display: flex;
        flex-direction: row;
        justify-content: center;
        margin:0 auto;
        padding-left: 0px;
    }
    li{
        font-size: 14px;
        margin:10px;
    }
    li:hover{
        cursor: pointer;
    }
    .active{
        color:chocolate;
        border-bottom: black solid 2px;
    }
</style>