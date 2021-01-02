<script>
    import Logo from '../../shared/Logo.svelte';
    import { Twitter, Github, Gmail} from "@icons-pack/svelte-simple-icons";

    let twitterLink = 'https://twitter.com/KamilRiyas';
    let githubLink = 'https://github.com/KamilRiyas';
    let gmailLink = "mailto: s.kamilriyas@gmail.com"
</script>

<logoHolder>
    <Logo socialLink={twitterLink}><Twitter color="#1DA1F2" size={25} /></Logo>
    <Logo socialLink={githubLink}><Github color="#211F1F" size={25} /></Logo>
    <Logo socialLink={gmailLink}><Gmail color="#D14836" size={25} /></Logo>
</logoHolder>

<style>
    logoHolder{
        list-style-type: none;
        display: flex;
        flex-direction: row;
    }
</style>