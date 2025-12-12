<script>
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div
	class="flex min-h-screen flex-col bg-brand-cream font-montserrat text-brand-brown selection:bg-brand-yellow selection:text-brand-brown"
>
	<Header />
	<main class="flex-1">
		{@render children()}
	</main>
	<Footer />
</div>
