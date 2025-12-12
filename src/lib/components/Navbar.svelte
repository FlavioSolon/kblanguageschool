<script>
	import StickerButton from './StickerButton.svelte';

	/** @type {{ name: string, href: string }[]} */
	const links = [
		{ name: 'Home', href: '/' },
		{ name: 'Quem Somos', href: '#quem-somos' },
		{ name: 'Por Que Escolher', href: '#por-que-escolher' }
	];

	let isMenuOpen = $state(false);

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<nav
	class="sticky top-0 z-50 w-full border-b-4 border-brand-brown bg-brand-purple px-6 py-4 shadow-[0px_4px_0px_rgba(0,0,0,1)]"
>
	<div class="mx-auto flex max-w-6xl items-center justify-between">
		<a
			href="/"
			class="font-display text-3xl tracking-wide text-brand-yellow drop-shadow-[2px_2px_0px_black] hover:scale-105 transition-transform"
		>
			KB SCHOOL
		</a>

		<!-- Desktop Menu -->
		<div class="hidden items-center gap-8 md:flex">
			{#each links as link}
				<a
					href={link.href}
					class="font-body text-lg font-bold text-white hover:text-brand-yellow hover:underline decoration-4 underline-offset-4 transition-all"
				>
					{link.name}
				</a>
			{/each}
			<StickerButton text="Matricule-se" color="yellow" link="/precos" />
		</div>

		<!-- Mobile Menu Button -->
		<button
			onclick={toggleMenu}
			class="md:hidden text-white font-bold border-2 border-white p-2 rounded bg-brand-pink shadow-[2px_2px_0px_black] active:translate-y-1 active:shadow-none"
		>
			MENU
		</button>
	</div>

	<!-- Mobile Menu Dropdown -->
	{#if isMenuOpen}
		<div
			class="absolute left-0 top-full w-full border-b-4 border-brand-brown bg-brand-cream p-6 shadow-xl md:hidden flex flex-col gap-4"
		>
			{#each links as link}
				<a
					href={link.href}
					class="font-display text-2xl text-brand-brown hover:text-brand-purple"
					onclick={toggleMenu}
				>
					{link.name}
				</a>
			{/each}
			<div
				class="contents"
				role="button"
				tabindex="0"
				onkeydown={(e) => e.key === 'Enter' && toggleMenu()}
				onclick={toggleMenu}
			>
				<StickerButton text="Matricule-se" color="yellow" link="/precos" />
			</div>
		</div>
	{/if}
</nav>
