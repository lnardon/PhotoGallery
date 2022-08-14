<script>
    import PhotoCard from "./PhotoCard.svelte"
    export let photos;
    export let title;
</script>

<div>
	<h2 class="title"> {title}</h2>
    <div class="container">
        {#each photos as photo}
        <PhotoCard url={photo.urls.small}/>
        {/each}
    </div>
</div>

<style>
    .container {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        width: 100%;
        max-width: 1440px;
    }

    .title {
        width: 100%;
        text-align: start;
        margin: 0rem 0rem 0rem 1rem
    }
</style>