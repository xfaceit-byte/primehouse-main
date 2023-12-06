<script>
	import { links } from '../constants';
	import { page } from '$app/stores';

	$: isHome = $page.url.pathname === '/';
	$: openMenu = false;

	const toggleMenu = () => {
		if (window.innerWidth < 1024) openMenu = !openMenu;
	};
</script>

<nav
	class="flex w-full justify-between bg-black px-8 pt-8 text-white lg:items-center lg:px-28"
	class:bg-transparent={isHome}
	class:pb-8={!isHome}
	class:absolute={isHome}
>
	<img src="primehouse-logo.svg" alt="primehouse logo" />
	<button
		class="left-0 right-0 top-[5vw] mx-auto hidden w-[90vw] list-none items-center justify-between space-y-6 rounded-xl bg-black/80 p-10 backdrop-blur-sm lg:pointer-events-none lg:static lg:mx-0 lg:ml-auto lg:flex lg:w-[50%] lg:space-y-0 lg:rounded-none lg:bg-transparent lg:p-0 lg:backdrop-blur-none xl:w-[40%]"
		class:hidden={!openMenu}
		class:absolute={openMenu}
		on:click={toggleMenu}
	>
		<p class="absolute right-5 top-5 lg:hidden">
			<img src="close.webp" alt="close icon" class="h-4 w-4 invert" />
		</p>
		{#each links as { name, path }}
			<li class="duration-200 hover:-rotate-2 hover:scale-110 hover:text-orange-400">
				<a
					href={path}
					class="pointer-events-auto text-xl font-medium"
					class:text-orange-400={$page.url.pathname === path}>{name}</a
				>
			</li>
		{/each}
	</button>
	<button on:click={toggleMenu} class:hidden={openMenu} class="h-fit lg:hidden"
		><img src="hamburger.png" alt="hamburger icon" class="h-8 w-8 invert" /></button
	>
	<div class:hidden={!openMenu} class="h-[53px]" />
</nav>
