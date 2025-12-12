<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div
	class="flex min-h-screen flex-col bg-brand-cream font-body text-brand-brown selection:bg-brand-yellow selection:text-brand-brown"
>
	<Navbar />
	<main class="flex-1">
		{@render children()}
	</main>
	<Footer />
</div>
