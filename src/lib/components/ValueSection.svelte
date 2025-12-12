<script>
	import StickerButton from './StickerButton.svelte';
	import HalftoneBackground from './HalftoneBackground.svelte';
</script>

<section class="relative overflow-hidden bg-brand-pink px-6 py-20">
	<HalftoneBackground color="brand-brown" />

	<div class="relative z-10 mx-auto grid max-w-6xl gap-12 md:grid-cols-2 items-center">
		<!-- Left: Image -->
		<div class="flex justify-center md:justify-end">
			<div
				class="relative w-full max-w-md aspect-square border-4 border-black hard-shadow overflow-hidden"
			>
				<img src="/keity_lendo.jpg" alt="Keity lendo um livro" class="w-full h-full object-cover" />
			</div>
		</div>

		<!-- Right: Text & CTA -->
		<div class="text-center md:text-left">
			<h2
				class="font-display text-5xl md:text-7xl text-white drop-shadow-[4px_4px_0px_black] leading-tight mb-8"
			>
				Aprenda a falar inglês com confiança
			</h2>

			<div class="flex justify-center md:justify-start">
				<StickerButton text="CONHEÇA NOSSOS PLANOS" link="/precos" color="yellow" />
			</div>
		</div>
	</div>
</section>
