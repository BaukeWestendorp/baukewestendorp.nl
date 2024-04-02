<script lang="ts">
	import '$lib/style.css';
	import { page } from '$app/stores';
	import { inject } from '@vercel/analytics';
	import { onMount } from 'svelte';
	onMount(() => {
		inject();
	});
</script>

<header>
	<a href="/"><h1>bauke westendorp.</h1></a>
	<nav>
		<a class:active={$page.url.pathname.startsWith('/portret')} href="/portret">portret</a>
		<a class:active={$page.url.pathname.startsWith('/band')} href="/band">band</a>
		<a class:active={$page.url.pathname.startsWith('/street')} href="/street">street</a>
		<a class:active={$page.url.pathname.startsWith('/sport')} href="/sport">sport</a>
	</nav>
</header>

<main>
	<slot />
</main>

<footer>
	<p class="copyright">© 2024 Bauke Westendorp</p>
</footer>

<style>
	header {
		padding: 1.5rem 2rem;

		display: flex;
		justify-content: space-between;
		align-items: baseline;
	}

	nav {
		display: flex;
		gap: 2rem;
	}

	h1 {
		font-size: 3rem;
	}

	a h1 {
		text-decoration: none;
	}

	.active {
		padding: 4px 8px;
		margin: -4px -8px;
		border-radius: 4px;
		outline: 1px solid var(--c-accent);
	}

	main {
		padding: 2rem;
	}

	footer {
		border-top: 1px solid var(--c-accent);
		padding: 1.5rem 2rem;
	}

	header,
	main,
	footer {
		width: 100%;
		max-width: var(--max-page-width);
		margin: 0 auto;
		box-sizing: border-box;
	}

	:global(body) {
		display: grid;
		grid-template-rows: auto 1fr auto;
		min-height: 100vh;
	}

	@media (max-width: 800px) {
		header {
			flex-direction: column;
			align-items: center;
			gap: 1rem;
		}

		header,
		main,
		footer {
			padding: 1rem;
		}

		h1 {
			font-size: 2rem;
		}
	}
</style>
