<script>
    import Logo from '../../shared/Logo.svelte';

    let twitterLogo = '/img/twitter-logo.webp';
    let githubLogo = '/img/github-logo.png';

    let twitterLink = 'https://twitter.com/KamilRiyas';
    let githubLink = 'https://github.com/KamilRiyas';
</script>

<logoHolder>
    <Logo logoPath={twitterLogo} socialLink={twitterLink} />
    <Logo logoPath={githubLogo} socialLink={githubLink} />
</logoHolder>

<style>
    logoHolder{
        list-style-type: none;
        display: flex;
        flex-direction: row;
    }
</style>