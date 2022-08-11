<script>
    import PhotoCard from "./PhotoCard.svelte"
    export let photos;
    export let title;
</script>

<div>
	<h2 class="title"> {title}</h2>
    <div class="container">
        {#each photos as photo}
        <PhotoCard url={photo.cover_photo.urls.small}/>
        {/each}
    </div>
</div>

<style>
    .container {
        display: flex;
        overflow-y: scroll;
        scroll-snap-type: x mandatory;
    }

    .title {
        width: 100%;
        text-align: start;
        margin: 0rem 0rem 0rem 1rem
    }
</style>