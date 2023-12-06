<script>
	import '../app.css';
	import Footer from './Footer.svelte';
	import Nav from './Nav.svelte';
</script>

<Nav />

<main>
	<slot />
</main>

<Footer />
