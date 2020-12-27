<script>
    import ProfilePicHolder from './ProfilePicHolder.svelte';
    import NavLogoHolder from './NavLogoHolder.svelte';
</script>

<header>
    <ProfilePicHolder />
    <NavLogoHolder />
</header>

<style>
    header{
        height: 100px;
        background-color: bisque;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
</style>
