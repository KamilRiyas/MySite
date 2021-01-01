<script>
    export let logoPath;
    export let socialLink;
</script>

<div class="logo">
    <a href={socialLink} target="_blank"><img src={logoPath} alt="Logo here"></a>
</div>

<style>
    .logo{
        display: flex;
        padding: 10px;
    }
    img{
        height: 30px;
        width: 30px;
        filter: grayscale(0.5);
    }
    img:hover{
        cursor: pointer;
    }
</style>