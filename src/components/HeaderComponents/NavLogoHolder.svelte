<script>
    import LogoHolder from './LogoHolder.svelte';
    import NavBar from './NavBar.svelte';
</script>

<header>
    <LogoHolder />
    <NavBar />
</header>

<style>
    header{
        height: 100px;
        background-color: bisque;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
</style>
