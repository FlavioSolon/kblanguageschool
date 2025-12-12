<script>
	const reasons = [
		'Aulas ao vivo',
		'Flexibilidade total',
		'Estude do celular'
	];
</script>

<section id="por-que-escolher" class="bg-brand-red px-6 py-20 border-t-4 border-brand-brown">
	<div class="mx-auto flex max-w-6xl flex-col items-center gap-12 md:flex-row">
		<!-- Left: Image -->
		<div class="flex-1 flex justify-center md:justify-end">
			<div
				class="sticker relative h-80 w-80 bg-brand-cream flex items-center justify-center rounded-full overflow-hidden border-4 border-white"
			>
				<img src="/aluna_pensando.jpg" alt="Aluna pensando" class="w-full h-full object-cover" />
			</div>
		</div>

		<!-- Right: Pills List -->
		<div class="flex-1 w-full">
			<h2
				class="font-anton mb-12 text-4xl uppercase text-brand-yellow drop-shadow-[3px_3px_0px_rgba(66,28,28,1)] md:text-6xl text-center md:text-left"
			>
				Por Que Escolher?
			</h2>

			<div class="flex flex-col gap-6 items-center md:items-start">
				{#each reasons as reason}
					<div
						class="hard-shadow inline-block rounded-full bg-brand-brown px-8 py-4 text-white transition-transform hover:-translate-y-1 hover:rotate-1"
					>
						<span class="font-display text-2xl uppercase tracking-wide">{reason}</span>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
