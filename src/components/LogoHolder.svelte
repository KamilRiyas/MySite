<script>
    import Logo from '../shared/Logo.svelte';

    let twitterLogo = '/img/twitter-logo.webp';
    let facebookLogo = '/img/facebook-logo.png';
    let githubLogo = '/img/github-logo.png';
    let profilePic = '/img/MyPic.jpg';
</script>

<logoHolder>
    <Logo logoPath={twitterLogo}/>
    <Logo logoPath={githubLogo}/>
    <Logo logoPath={facebookLogo}/>
</logoHolder>

<style>
    logoHolder{
        list-style-type: none;
        display: flex;
        flex-direction: row;
    }
</style>