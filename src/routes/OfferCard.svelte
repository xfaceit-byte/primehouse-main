<script>
	export let offerData;

	const { title, oldPrice, newPrice, city, img } = offerData;
</script>

<div class="w-[350px] overflow-hidden rounded-3xl bg-white text-left">
	<img src={img} alt="offer" class="h-44 w-full object-cover" />
	<div class="p-5">
		<h2 class="mb-1 font-bold">{title}</h2>
		<h3 class:hidden={!oldPrice} class="mr-2 inline font-semibold text-red-500 line-through">
			{oldPrice}
		</h3>
		<h3 class="inline font-bold text-yellow-600">{newPrice}</h3>
		<p>{city}</p>
	</div>
</div>
