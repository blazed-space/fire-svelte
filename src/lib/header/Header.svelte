<script>
    import Nav from "$lib/nav/Nav.svelte";
    export let burgerOpened = false;
    function toggleMenu(){
        if(burgerOpened == true){
            burgerOpened = false;
        } else {
            burgerOpened = true;
        }
    }
</script>

<header class="p-4 bg-gray-100 text-gray-800">
	<div class="container flex justify-between h-16 mx-auto">
		<a rel="noopener noreferrer" title="Fire for Svelte" href="#" aria-label="Back to homepage" class="flex items-center p-2 hover:opacity-75">
			<img src="https://blazed.sirv.com/logo/Beaker-Cobalt.png?w=50&h=50" alt="Logo" />
		</a>
		<div>
			<!-- Desktop Menu -->
			<ul class="items-stretch hidden space-x-3 md:flex mt-3">
				<Nav />
			</ul>
		</div>
		<!-- Mobile menu button -->
		<div class="flex md:hidden">
			<button on:click={toggleMenu} type="button" class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400" aria-label="toggle menu">
				{#if !burgerOpened}
					<svg viewBox="0 0 24 24" class="w-9 h-9 fill-current">
						<path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
					</svg>
				{:else}
					<svg class="w-10 h-10 fill-current" width="50" height="50" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.646 5.646a.5.5 0 000 .708l8 8a.5.5 0 00.708-.708l-8-8a.5.5 0 00-.708 0z" clip-rule="evenodd"/>
						<path fill-rule="evenodd" d="M14.354 5.646a.5.5 0 010 .708l-8 8a.5.5 0 01-.708-.708l8-8a.5.5 0 01.708 0z" clip-rule="evenodd"/>
					</svg>
				{/if}
			</button>
		</div>
	</div>
	<div>
		{#if burgerOpened}
			<!-- Mobile Menu -->
			<ul class="relative mobile-menu">
				<Nav />
			</ul>
		{/if}
	</div>
</header>
<style>
	.mobile-menu{
        display:none;
    }
    @media screen and (max-width: 768px){
        .mobile-menu{
            display:block;
        }
        .desktop-menu{
            display:none;
        }
    }
</style>