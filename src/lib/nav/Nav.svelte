<script>
	import { page } from '$app/stores';
</script>
<li class="block lg:flex">
    <a rel="noopener noreferrer" sveltekit:prefetch href="/" class:active={$page.url.pathname === '/'} class="block lg:flex text-center items-center px-4 py-3 -mb-1 border-b-2 border-transparent text-gray-700">
        Home
    </a>
</li>
<li class="lg:flex">
    <a rel="noopener noreferrer" sveltekit:prefetch href="/about" class:active={$page.url.pathname === '/about'} class="block lg:flex text-center items-center px-4 py-3 -mb-1 border-b-2 border-transparent text-gray-700">
        About
    </a>
</li>
<li class="lg:flex">
    <a rel="noopener noreferrer" sveltekit:prefetch href="/todos" class:active={$page.url.pathname === '/todos'} class="block lg:flex text-center items-center px-4 py-3 -mb-1 border-b-2 border-transparent text-gray-700">
        Todos
    </a>
</li>
<style>
    .active{
		text-decoration: underline;
	}
</style>