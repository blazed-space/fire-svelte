<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main class="pt-10">
	<slot />
</main>

<hr />

<footer class="bg-white">
	<p>
		&bull; Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit.
	</p>
	<p>
		&bull; Visit <a href="https://github.com/blazed-space/fire-svelte">Fire Svelte Repository</a> to learn Fire for Svelte.
	</p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
