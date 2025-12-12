<script>
	import StickerButton from '$lib/components/StickerButton.svelte';
	import HalftoneBackground from '$lib/components/HalftoneBackground.svelte';
	import { fly } from 'svelte/transition';

	const individualPackages = [
		{ hours: '1h', semester: '370', annual: '341' },
		{ hours: '1h30', semester: '518', annual: '481' },
		{ hours: '2h', semester: '665', annual: '608' }
	];

	const groupPackages = [
		{ hours: '1h', semester: '220' },
		{ hours: '1h30', semester: '331' },
		{ hours: '2h', semester: '441' }
	];
</script>

<svelte:head>
	<title>Preços - KB Language School</title>
</svelte:head>

<!-- Header -->
<header class="relative overflow-hidden bg-brand-red px-6 py-20 text-center">
	<!-- Scribble Texture Overlay (CSS approximation) -->
	<div
		class="absolute inset-0 opacity-10 pointer-events-none"
		style="background-image: repeating-linear-gradient(45deg, #000 0, #000 1px, transparent 0, transparent 50%); background-size: 20px 20px;"
	></div>

	<div class="relative z-10">
		<h1 class="font-display text-6xl text-brand-yellow drop-shadow-[4px_4px_0px_black] md:text-8xl">
			PACOTES DE AULAS
		</h1>
		<p class="mt-4 font-hand text-3xl text-white md:text-4xl">Do zero à fluência, no seu ritmo!</p>
	</div>
</header>

<!-- Group 1: Individual Packages -->
<section class="relative bg-brand-purple px-6 py-20">
	<HalftoneBackground color="brand-yellow" />

	<div class="relative z-10 mx-auto max-w-6xl">
		<h2 class="mb-12 text-center font-display text-4xl text-white drop-shadow-[3px_3px_0px_black]">
			PACOTES INDIVIDUAIS
		</h2>

		<div class="grid gap-8 md:grid-cols-3">
			{#each individualPackages as pkg, i}
				<div
					in:fly={{ y: 50, duration: 800, delay: i * 200 }}
					class="sticker flex flex-col items-center bg-brand-yellow p-8 text-center transition-transform hover:-translate-y-2"
				>
					<h3 class="font-display text-5xl text-brand-purple mb-2">{pkg.hours}</h3>
					<span class="font-body text-sm font-bold uppercase tracking-wide text-brand-brown mb-6"
						>Semanal</span
					>

					<div class="w-full space-y-6">
						<div class="border-b-2 border-brand-brown pb-4">
							<p class="font-body text-sm font-bold text-brand-brown">Semestral (25 semanas)</p>
							<p class="font-display text-3xl text-brand-red">
								<span class="text-lg align-top">6x R$</span>{pkg.semester}
							</p>
						</div>
						<div>
							<p class="font-body text-sm font-bold text-brand-brown">Anual (50 semanas)</p>
							<p class="font-display text-3xl text-brand-red">
								<span class="text-lg align-top">12x R$</span>{pkg.annual}
							</p>
						</div>
					</div>

					<div class="mt-8">
						<StickerButton text="Eu Quero" color="purple" />
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Group 2: Group Packages -->
<section class="bg-brand-cream px-6 py-20 border-t-4 border-brand-brown">
	<div class="mx-auto max-w-6xl">
		<h2
			class="mb-12 text-center font-display text-4xl text-brand-brown drop-shadow-[2px_2px_0px_rgba(0,0,0,0.2)]"
		>
			TURMAS A PARTIR DE 4 PESSOAS
		</h2>

		<div class="grid gap-8 md:grid-cols-3">
			{#each groupPackages as pkg}
				<div
					class="flex flex-col items-center rounded-3xl border-4 border-brand-brown p-8 text-center transition-colors hover:bg-white"
				>
					<h3 class="font-display text-5xl text-brand-brown mb-2">{pkg.hours}</h3>
					<span class="font-body text-sm font-bold uppercase tracking-wide text-brand-brown mb-6"
						>Semanal</span
					>

					<div class="w-full">
						<p class="font-body text-sm font-bold text-brand-brown">Semestral (25 semanas)</p>
						<p class="font-display text-4xl text-brand-orange mt-2">
							<span class="text-lg align-top">6x R$</span>{pkg.semester}
						</p>
					</div>

					<div class="mt-8">
						<StickerButton text="Matricular" color="orange" />
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Group 3: Custom Banner -->
<section class="bg-brand-orange px-6 py-16 text-center border-t-4 border-brand-brown">
	<div class="mx-auto max-w-4xl">
		<h2 class="font-display text-4xl text-white drop-shadow-[3px_3px_0px_black] mb-8 md:text-5xl">
			Precisa de carga horária maior?
		</h2>
		<StickerButton
			text="FALE COM A GENTE"
			link="https://wa.me/5511999999999"
			color="white"
			class="text-brand-orange"
		/>
	</div>
</section>
