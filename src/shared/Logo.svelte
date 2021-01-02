<script>
    export let socialLink;
</script>

<div class="logo">
    <a href={socialLink} target="_blank"><slot></slot></a>
</div>

<style>
    .logo{
        display: flex;
        padding: 10px;
    }
</style>