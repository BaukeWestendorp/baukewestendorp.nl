<script lang="ts">
	import ImageGrid from '$lib/components/ImageGrid.svelte';
</script>

<svelte:head>
	<title>Fotografie</title>
</svelte:head>

<article>
	<h1>Fotografie</h1>

	<ImageGrid folder="photos" alt="Photos" />
</article>

<style>
	h1 {
		margin-bottom: 2rem;
	}

	article {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
</style>
