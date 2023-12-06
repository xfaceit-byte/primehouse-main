<script>
	export let houseData;

	let { style, localitatea, img, bedrooms, showers, total } = houseData;
</script>

<div
	class="w-fit rounded-3xl bg-white shadow-2xl duration-200 hover:scale-105 hover:text-orange-400"
>
	<img src={img} alt={style} class="w-full object-cover" />
	<h4 class="px-3 py-6 text-center text-xl font-bold">
		{style} - {localitatea}
	</h4>
	<div class="flex justify-between">
		<p class="flex w-full gap-2 border-t px-10 py-4 font-medium">
			<img src="bed.svg" alt="bed icon" />
			{bedrooms}
		</p>
		<p class="flex w-full gap-2 border-t px-10 py-4 font-medium">
			<img src="shower.svg" alt="shower icon" />
			{showers}
		</p>
		<p class="flex w-full gap-2 border-t px-10 py-4 font-medium">
			<img src="camere.svg" alt="camere icon" />
			{total}
		</p>
	</div>
</div>
