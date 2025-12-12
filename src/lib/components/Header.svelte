<script>
	/** @type {{ name: string, href: string }[]} */
	const links = [
		{ name: 'Home', href: '/' },
		{ name: 'Quem Somos', href: '#quem-somos' },
		{ name: 'Por Que Escolher', href: '#por-que-escolher' },
		{ name: 'Destaques', href: '#destaques' }
	];
</script>

<header class="sticky top-0 z-50 w-full border-b-4 border-brand-brown bg-brand-cream px-6 py-4 hard-shadow">
	<div class="mx-auto flex max-w-6xl items-center justify-between">
		<a href="/" class="font-anton text-3xl tracking-wide text-brand-purple drop-shadow-[2px_2px_0px_rgba(0,0,0,1)] hover:scale-105 transition-transform">
			KB SCHOOL
		</a>

		<nav class="hidden md:flex gap-8">
			{#each links as link}
				<a
					href={link.href}
					class="font-montserrat text-lg font-bold text-brand-brown hover:text-brand-pink hover:underline decoration-4 underline-offset-4 transition-all"
				>
					{link.name}
				</a>
			{/each}
		</nav>

		<!-- Mobile Menu Button Placeholder -->
		<button class="md:hidden text-brand-brown font-bold border-2 border-brand-brown p-2 rounded bg-brand-yellow hard-shadow">
			MENU
		</button>
	</div>
</header>
