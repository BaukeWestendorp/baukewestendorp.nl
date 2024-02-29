<script lang="ts">
	export let folder: 'band' | 'portret' | 'street' | 'sport';
	export let alt: string;

	const allImageModules = {
		band: import.meta.glob('$lib/img/band/*.{avif,gif,heif,jpeg,jpg,png,tiff,webp}', {
			query: {
				enhanced: true
			},
			eager: true
		}),
		portret: import.meta.glob('$lib/img/portret/*.{avif,gif,heif,jpeg,jpg,png,tiff,webp}', {
			query: {
				enhanced: true
			},
			eager: true
		}),
		street: import.meta.glob('$lib/img/street/*.{avif,gif,heif,jpeg,jpg,png,tiff,webp}', {
			query: {
				enhanced: true
			},
			eager: true
		}),
		sport: import.meta.glob('$lib/img/sport/*.{avif,gif,heif,jpeg,jpg,png,tiff,webp}', {
			query: {
				enhanced: true
			},
			eager: true
		})
	};
	const imageModules = allImageModules[folder];

	const images = Object.values(imageModules).map((module) => (module as any).default);
</script>

<div class="image-grid">
	{#each images as image}
		<enhanced:img class="image loading" src={image} {alt} />
	{/each}
</div>

<style>
	.image-grid {
		/* Prevent vertical gaps */
		line-height: 0;

		-webkit-column-count: 2;
		-webkit-column-gap: var(--image-grid-gap);
		-moz-column-count: 2;
		-moz-column-gap: var(--image-grid-gap);
		column-count: 2;
		column-gap: var(--image-grid-gap);
	}

	.image-grid .image {
		/* Just in case there are inline attributes */
		width: 100% !important;
		height: auto !important;

		margin-bottom: var(--image-grid-gap);
	}

	@media (max-width: 800px) {
		.image-grid {
			-moz-column-count: 1;
			-webkit-column-count: 1;
			column-count: 1;
		}
	}
</style>
