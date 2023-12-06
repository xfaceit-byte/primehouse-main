<script>
	import { houseDesigns } from '../../constants';
	import HouseCard from './HouseCard.svelte';
</script>

<section class="bg-gray-100">
	<div class="flex flex-col items-center justify-between gap-16 lg:flex-row">
		<hr class="h-2 w-full bg-gradient-to-r from-yellow-400 to-orange-400" />
		<h2 class="text-right text-4xl font-bold lg:w-[900px] lg:text-6xl">
			<span class="text-orange-400">Exterior</span>
			design
		</h2>
	</div>
	<div class="mt-20 grid place-items-center gap-10 md:grid-cols-2 xl:grid-cols-3">
		{#each houseDesigns.exterior as house}
			<HouseCard houseData={house} />
		{/each}
	</div>
</section>

<section>
	<div class="flex flex-col items-center justify-between gap-16 lg:flex-row">
		<h2 class="text-right text-4xl font-bold lg:w-[900px] lg:text-6xl">
			<span class="text-orange-400">Interior</span>
			design
		</h2>
		<hr class="h-2 w-full bg-gradient-to-r from-yellow-400 to-orange-400" />
	</div>
	<div class="mt-20 grid place-items-center gap-10 md:grid-cols-2 xl:grid-cols-3">
		{#each houseDesigns.interior as house}
			<HouseCard houseData={house} />
		{/each}
	</div>
</section>
