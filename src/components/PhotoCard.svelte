<script>
    export let url;
</script>

<div class="container">
    <img src={`${url}`} alt="">
</div>

<style>
    img {
        display: block;
        width: 100%;
        max-width: 300px;
        height: 250px;
        object-fit: cover;
        width: max-content;
        border-radius: 0.25rem;
    }

    .container {
        margin: 2rem 1rem;
        scroll-snap-align: start;
        cursor: pointer;
    }
</style>