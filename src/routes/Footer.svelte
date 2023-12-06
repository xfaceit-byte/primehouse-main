<script>
	import { links } from '../constants';
	import { page } from '$app/stores';
</script>

<footer class="bg-gradient-to-tr from-[#050505] to-[#b6531c] p-8 py-16 text-white lg:p-16">
	<h2
		class="mb-12 text-center text-3xl font-bold lg:text-5xl"
		class:hidden={$page.url.pathname !== '/'}
	>
		Make your dreams a <span class="text-orange-400">reality</span>
	</h2>
	<hr class="mb-12 opacity-20" />
	<div
		class="flex flex-col-reverse place-items-center justify-between gap-16 lg:flex-row lg:gap-0 lg:px-28"
	>
		<div>
			<img src="primehouse-logo.svg" alt="primehouse logo" />
			<div class="mt-2 flex justify-between">
				<a href="https://www.facebook.com/" target="_blank">
					<img src="facebook.svg" alt="facebook icon" />
				</a>
				<a href="https://www.twitter.com/" target="_blank">
					<img src="twitter.svg" alt="twiter icon" />
				</a>
				<a href="https://www.instagram.com/" target="_blank">
					<img src="instagram.svg" alt="instagram icon" />
				</a>
			</div>
		</div>
		<div>
			<h3>Customer Service</h3>
			<a
				href="https://www.freeprivacypolicy.com/live/289697ba-bdf8-4ad2-8542-4176186cc338"
				target="_blank">Privacy Policy</a
			>
			<a
				href="https://www.freeprivacypolicy.com/live/289697ba-bdf8-4ad2-8542-4176186cc338"
				target="_blank">Shipping Policy</a
			>
			<a
				href="https://www.freeprivacypolicy.com/live/25ac9fdc-22de-496a-bda6-640eb7c6de17"
				target="_blank">Cookies Policy</a
			>
			<a
				href="https://www.freeprivacypolicy.com/live/a97e84c4-5d41-4ad7-b3ae-0b40928fc9a5"
				target="_blank">Terms of Service</a
			>
			<a
				href="https://www.freeprivacypolicy.com/live/3241c910-74ed-4500-99c1-a40096f9563b"
				target="_blank">Legal Notes</a
			>
		</div>
		<div>
			<h3>Information</h3>
			<a href="">About Us</a>
			<a href="">Help Center</a>
			<a href="">New Suppliers</a>
			<a href="">Product Recalls</a>
			<a href="">Contact Us</a>
		</div>
		<div style="margin-bottom: 2%;">
			<h3>Pages</h3>
			{#each links as { name, path }}
				<a href={path}>{name}</a>
			{/each}
		</div>
	</div>
</footer>

<style lang="postcss">
	a {
		@apply block;
	}
	h3 {
		@apply mb-5 text-xl font-bold;
	}
	footer > div > div {
		@apply text-center lg:text-left;
	}
</style>
