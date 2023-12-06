<script>
	import { clients, offers } from '../constants';
	import OfferCard from './OfferCard.svelte';
</script>

<section
	class="text-shadow flex h-screen flex-col justify-center bg-[url('/house-background.jpg')] bg-cover bg-center pb-40 text-white lg:bg-left"
>
	<h1 class="mt-20 text-5xl font-bold lg:max-w-[50%] lg:text-7xl">
		Find your dream
		<span class="text-orange-400">home</span>
		today
	</h1>
	<p class="text-shadow my-5 lg:max-w-[50%]">
		Discover your dream home today! With our assistance, finding the perfect home for you is quick
		and easy. We offer a diverse range of top-notch properties, suitable for all tastes and budgets.
	</p>
</section>

<section class="grid place-items-center items-center gap-7 lg:flex lg:gap-14">
	<img src="interior.jpg" alt="" class="rounded-[40px] lg:-ml-28 lg:w-[40%] lg:rounded-none" />
	<div class="space-y-10">
		<hr class="-mb-5 h-2 w-28 bg-gradient-to-r from-yellow-400 to-orange-400" />
		<h2 class="text-4xl font-bold lg:text-6xl">
			Experts in <span class="text-orange-400">interior design</span>
		</h2>
		<p>
			Discover the art of interior design! Let us transform your space into a harmonious blend of
			style and functionality. From color palettes to furniture choices, we create interiors that
			reflect your personality and provide a true sense of home.
		</p>
		<a
			href="/catalogs"
			class="block w-fit rounded-r-2xl bg-orange-500 px-5 py-5 text-lg font-bold text-white duration-200 hover:bg-orange-400"
		>
			See our catalog →
		</a>
	</div>
</section>

<section class="bg-gradient-to-r from-yellow-100 to-orange-100">
	<h2 class="text-center text-4xl font-bold lg:text-6xl">
		Top <span class="text-orange-400">offers</span> around the world
	</h2>
	<p class="mt-5 text-center">
		Fulfill your career dreams, enjoy all the achievements of the city center and luxury housing to
		the fullest.
	</p>
	<p class="mt-5 text-center">The most beautiful interior designs we made around the world.</p>
	<ul
		class="custom-scrollbar -ml-10 mb-2 flex w-[102.5vw] list-none items-center gap-10 overflow-x-scroll px-3 pb-14 pt-16 text-center lg:-ml-28 lg:w-[99vw] lg:px-10"
	>
		{#each offers as offer}
			<li>
				<OfferCard offerData={offer} />
			</li>
		{/each}
	</ul>
</section>

<section>
	<h2 class="text-center text-4xl font-bold lg:text-6xl">
		OUR <span class="text-orange-400">BIGGEST</span> PROJECT
	</h2>
	<iframe
		src="https://www.youtube.com/embed/N_52j2JxkBs?si=qh1XhQeLaQ5zOdpY"
		title="YouTube video player"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
		allowfullscreen
		class="mx-auto mt-10 h-[46vw] w-full lg:h-[34vw] lg:w-[60vw]"
	></iframe>
</section>

<section class="grid place-items-center bg-gray-100">
	<div class="mb-10 lg:w-[50%]">
		<hr class="mb-10 h-2 w-full bg-gradient-to-r from-yellow-400 to-orange-400" />
		<p class="text-center text-lg">
			„Exceptional interior design service! From concept to execution, they seamlessly combined
			style and functionality, creating a space that truly feels like home. I highly recommend their
			expertise for anyone seeking a personalized and aesthetic touch to their living spaces.”
		</p>
	</div>
	<div class="grid gap-10 lg:grid-cols-3">
		{#each clients as { image, name }}
			<div class="bg-black px-28 py-8 text-white">
				<img src={image} alt={name} />
				<h3 class="mt-3 text-center">{name}</h3>
			</div>
		{/each}
	</div>
</section>

<style>
	.custom-scrollbar::-webkit-scrollbar {
		height: 8px;
	}
	.custom-scrollbar::-webkit-scrollbar-thumb {
		background-color: rgb(251 146 60);
		border-radius: 20px;
	}
	.text-shadow {
		text-shadow: 0 0 70px black;
	}
	@media (max-width: 1024px) {
		li:last-child {
			margin-right: -6px;
		}
	}
</style>
