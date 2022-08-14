<script>
	import PhotoRow from "./components/PhotoRow.svelte"
	let response;
	fetch(`https://api.unsplash.com/search/photos/?page=1&per_page=50&orientation=landscape&query=planets&client_id=${process.env.API_KEY}`)
	.then(response => response.json())
	.then(parsed => response = parsed.results)
</script>

<main>
	<h1>Photo<br>Gallery</h1>
	{#if response}
	<PhotoRow photos={response} title="Space"/>
	{/if}
	
</main>

<style>
	main {
		text-align: center;
		width: 100%;
		min-height: 100vh;
		background-color: #131313;
		color: #fafafa;
		overflow: hidden;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
		padding: 3rem 0rem;
	}
</style>