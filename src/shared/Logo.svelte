<script>
    export let logoPath;
</script>

<div class="logo">
    <img src={logoPath} alt="Logo here">
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
</style>