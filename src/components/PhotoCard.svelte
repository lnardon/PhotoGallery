<script>
    export let url;
</script>

<div class="container">
    <img src={`${url}`} alt="">
</div>

<style>
    img {
        display: block;
        height: 150px;
        width: max-content;
    }

    .container {
        margin: 2rem 1rem;
        scroll-snap-align: start;
    }
</style>