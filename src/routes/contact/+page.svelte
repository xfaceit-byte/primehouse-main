<section class="space-y-4">
	<h1 class="text-4xl font-bold lg:text-5xl">
		Contact your
		<span class="text-orange-400">Prime</span>
		commercial real estate agent
	</h1>
	<p>
		Our commercial real estate advisors are here to help you with your next project or big decision.
		Simply fill out the form below and someone will get back to you as soon as possible.
	</p>
</section>

<hr class="-my-8 mx-auto h-2 w-[50%] bg-gradient-to-r from-yellow-400 to-orange-400" />

<section class="flex flex-col gap-16 lg:flex-row lg:gap-32">
	<form action="" class="w-fit space-y-5">
		<div class="grid-cols-2 gap-x-14">
			<label for="first">*First name</label>
			<label for="last">*Last name</label>
			<input type="text" name="first" />
			<input type="name" name="last" />
		</div>
		<div>
			<label for="email">*Email</label>
			<input type="email" name="email" />
		</div>
		<div>
			<label for="phone">*Phone number</label>
			<input type="tel" name="phone" />
		</div>
		<div>
			<label for="company">*Company name (optional)</label>
			<input type="text" name="company" />
		</div>
		<p class="max-w-[560px] text-sm">
			Prime needs the contact information you provide to us to contact you about our services. You
			may unsubscribe from these communications at any time. For information on how to unsubscribe,
			as well as our privacy practices and commitment to protecting your privacy, check out our
			Privacy Policy.
		</p>
		<button
			type="submit"
			class="mx-auto block w-fit border-2 border-black bg-gray-100 px-10 py-3 duration-200 hover:bg-gray-300"
			>SUBMIT</button
		>
	</form>
	<div class="space-y-5">
		<h3 class="text-3xl">Other ways to reach to us</h3>
		<a href="https://www.facebook.com/" target="_blank">
			<img src="facebook.svg" alt="facebook icon" />
			Facebook
		</a>
		<a href="https://www.twitter.com/" target="_blank">
			<img src="twitter.svg" alt="twiter icon" />
			Twitter
		</a>
		<a href="https://www.instagram.com/" target="_blank">
			<img src="instagram.svg" alt="instagram icon" />
			Instagram
		</a>
	</div>
</section>

<style lang="postcss">
	form > div {
		@apply grid gap-y-1;
	}
	input {
		@apply h-8 border-2 border-black;
	}
	img {
		@apply h-5 w-5 invert;
	}
	a {
		@apply flex items-center gap-4 text-lg italic duration-200 hover:text-orange-400;
	}
</style>
