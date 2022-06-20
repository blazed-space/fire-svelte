<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<script>
	export let pageTitle = "About Fire for SvelteKit";
	export let pageDesc = "A boilerplate framework for SvelteKit.";
</script>

<svelte:head>
	<title>
		{pageTitle}
	</title>
	<meta name="twitter:title" content={pageTitle}>
	<meta property="og:title" content={pageTitle}>
	<meta name="description" content={pageDesc} />
	<meta name="twitter:description" content={pageDesc}>
	<meta property="og:description" content={pageDesc}>
	<meta itemprop="description" content={pageDesc}>
</svelte:head>

<div class="content">
	<h1 class="mb-5">
		About this app
	</h1>

	<p>
		This is a <a href="https://kit.svelte.dev">SvelteKit</a> app. You can make your own by typing the
		following into your command line and following the prompts:
	</p>

	<pre>npm init svelte</pre>

	<p>
		The page you're looking at is purely static HTML, with no client-side interactivity needed.
		Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
		the devtools network panel and reloading.
	</p>

	<p class="mb-10">
		The <a href="/todos">TODOs</a> page illustrates SvelteKit's data loading and form handling. Try using
		it with JavaScript disabled!
	</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
