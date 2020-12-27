<script>
    import {activeNav, activeSubNav} from '../../stores/navigationStore.js';

    let homeNavs = ['Profession','Passion','Interest'];
    let activeMenu = 'Profession';
    let activeSubMenu;

    const handleClick = (e) => {
        //update the store about the active element
        activeNav.update(value => e.srcElement.innerText);
        //update the UI to show the active menu
        activeMenu = e.srcElement.innerText;
        //update subnav according to the selected Main nav item
        switch (activeMenu) {
            case 'Profession':
                activeSubMenu = 'Expertise';
                break;
            case 'Passion':
                activeSubMenu = 'Hiking';
                break;
            case 'Interest':
                activeSubMenu = 'Music';
                break;
            default:
                break;
        }
        activeSubNav.update(value => activeSubMenu);
    }
</script>

<navbar>
    <ul>
        {#each homeNavs as nav}
            <li on:click={e => handleClick(e)} class:active={nav === activeMenu}>{nav}</li>
        {/each}
    </ul>
</navbar>

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