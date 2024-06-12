<script>
	let email = '';
	let password = '';
	let errorMessage = '';
	let successMessage = '';
	let showModal = false;
	let modalMessage = '';

	const validUsers = [
		{ email: 'tuzovmax26@gmail.com', password: 'max123' },
		{ email: 'user2@example.com', password: 'password2' },
		{ email: 'user3@example.com', password: 'password3' }
	];

	const handleSubmit = () => {
		const user = validUsers.find((user) => user.email === email && user.password === password);
		if (user) {
			successMessage = 'Login successful!';
			errorMessage = '';
			modalMessage = 'Login successful!';
			showModal = true;
		} else {
			errorMessage = 'Invalid email or password';
			successMessage = '';
			modalMessage = 'Invalid email or password';
			showModal = true;
		}
	};

	const closeModal = () => {
		showModal = false;
		if (modalMessage === 'Login successful!') {
			window.location.href = '/';
		}
	};
</script>

<div class="container">
	<div class="form-wrapper">
		<h1 class="font-semibold">Login to <span class="text-orange-500">PrimeHouse</span></h1>
		<form on:submit|preventDefault={handleSubmit}>
			<input type="email" bind:value={email} placeholder="Email" required />
			<input type="password" bind:value={password} placeholder="Password" required />
			<button type="submit">Login</button>
		</form>
		{#if errorMessage}
			<p class="message error">{errorMessage}</p>
		{/if}
		{#if successMessage}
			<p class="message success">{successMessage}</p>
		{/if}
		<p>Don't have an account? <a href="/register">Sign up</a></p>
	</div>

	{#if showModal}
		<div class="fixed inset-0 flex items-center justify-center bg-gray-800 bg-opacity-75">
			<div class="w-full max-w-sm rounded bg-white p-6 text-center shadow-lg">
				<p class="mb-4">{modalMessage}</p>
				<button
					on:click={closeModal}
					class="rounded bg-orange-500 px-4 py-2 text-white transition duration-200 hover:bg-orange-600"
					>OK</button
				>
			</div>
		</div>
	{/if}
</div>

<style>
	.container {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		background: url('https://images5.alphacoders.com/134/1347174.png') no-repeat center center/cover;
		font-family: 'Arial', sans-serif;
	}

	.form-wrapper {
		background: white;
		padding: 2rem 3rem;
		border-radius: 10px;
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
		max-width: 400px;
		width: 100%;
		text-align: center;
		animation: fadeIn 1s ease-in-out;
	}

	@keyframes fadeIn {
		from {
			opacity: 0;
			transform: translateY(-20px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	h1 {
		margin-bottom: 1.5rem;
		color: #333;
		font-size: 2rem;
	}

	input {
		width: calc(100% - 2rem);
		padding: 0.75rem 1rem;
		margin: 0.5rem 0;
		border: 1px solid #ddd;
		border-radius: 5px;
		font-size: 1rem;
		transition: border-color 0.3s;
	}

	input:focus {
		border-color: #ff7e5f;
		outline: none;
	}

	button {
		width: calc(100% - 2rem);
		padding: 0.75rem 1rem;
		margin: 1rem 0;
		background-color: #ff7e5f;
		border: none;
		border-radius: 5px;
		color: white;
		font-size: 1rem;
		cursor: pointer;
		transition: background 0.3s;
	}

	button:hover {
		background-color: #e06b50;
	}

	.form-wrapper p {
		margin-top: 1rem;
		color: #666;
	}

	.form-wrapper a {
		color: #ff7e5f;
		text-decoration: none;
		transition: color 0.3s;
	}

	.form-wrapper a:hover {
		color: #e06b50;
	}

	.message {
		margin-top: 1rem;
		font-size: 1rem;
	}

	.error {
		color: #ff4d4f;
	}

	.success {
		color: #52c41a;
	}

	.fixed {
		position: fixed;
	}

	.inset-0 {
		top: 0;
		right: 0;
		bottom: 0;
		left: 0;
	}

	.bg-gray-800 {
		background-color: rgba(31, 41, 55, 1);
	}

	.bg-opacity-75 {
		background-opacity: 0.75;
	}

	.p-6 {
		padding: 1.5rem;
	}

	.rounded {
		border-radius: 0.375rem;
	}

	.shadow-lg {
		box-shadow:
			0 10px 15px -3px rgba(0, 0, 0, 0.1),
			0 4px 6px -2px rgba(0, 0, 0, 0.05);
	}

	.text-center {
		text-align: center;
	}

	.max-w-sm {
		max-width: 24rem;
	}

	.bg-white {
		background-color: white;
	}

	.text-white {
		color: white;
	}

	.hover\:bg-orange-600:hover {
		background-color: #e06b50;
	}

	.transition {
		transition-property: all;
		transition-duration: 200ms;
	}

	.duration-200 {
		transition-duration: 200ms;
	}
</style>
