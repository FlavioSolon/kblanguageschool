<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<title>KB Language School - Aprenda Inglês com Estilo</title>
	<meta
		name="description"
		content="Aprenda idiomas de forma acessível, personalizada e prática. Aulas online, ao vivo e com metodologia focada em conversação."
	/>
	<meta property="og:title" content="KB Language School - Aprenda Inglês com Estilo" />
	<meta
		property="og:description"
		content="Aprenda idiomas de forma acessível, personalizada e prática. Aulas online, ao vivo e com metodologia focada em conversação."
	/>
	<meta property="og:image" content="https://kblanguageschool.vercel.app/og-image.png" />
	<meta property="og:type" content="website" />
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
