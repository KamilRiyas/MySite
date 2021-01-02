<script>
    import ProfilePicHolder from './ProfilePicHolder.svelte';
    import NavLogoHolder from './NavLogoHolder.svelte';

    import MediaQuery from 'svelte-media-query';
</script>

<header>
    <ProfilePicHolder />
    <NavLogoHolder />
</header>

<style>
    header{
        width: 100%;
        height: 100px;
        background-color: bisque;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
</style>
