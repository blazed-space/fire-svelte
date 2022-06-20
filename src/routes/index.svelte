<script>
	export let pageTitle = "Fire for SvelteKit";
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
	<div class="py-6 text-gray-900">
		<div class="container mx-auto flex flex-col items-center justify-center p-4 space-y-8 md:p-10 md:px-24 xl:px-48">
			<h1 class="text-5xl font-bold leading-none text-center">
				Welcome to Fire for SvelteKit
			</h1>
			<p class="text-xl font-medium text-center">
				Try editing <strong>src/routes/index.svelte</strong>
			</p>
			<div class="flex flex-col space-y-4 sm:space-y-0 sm:flex-row sm:space-x-8">
				<a href="https://github.com/blazed-space/fire-svelte" target="_blank" class="px-8 py-3 text-lg font-semibold rounded bg-blue-600 hover:bg-blue-700 text-gray-50">
					Repository
				</a>
			</div>
		</div>
	</div>
</div>
