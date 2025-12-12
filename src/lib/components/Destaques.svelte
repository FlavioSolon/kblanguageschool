<script>
	const highlights = [
		{ title: 'Inglês para Viagem', tag: 'Rápido' },
		{ title: 'Conversação Avançada', tag: 'Fluência' },
		{ title: 'Preparatório TOEFL', tag: 'Foco' }
	];
</script>

<section id="destaques" class="bg-brand-yellow px-6 py-20 border-t-4 border-brand-brown">
	<div class="mx-auto max-w-6xl">
		<h2
			class="font-anton mb-12 text-center text-4xl uppercase text-brand-purple drop-shadow-[3px_3px_0px_rgba(255,255,255,1)] md:text-6xl"
		>
			Destaques
		</h2>

		<div class="flex flex-wrap justify-center gap-8">
			{#each highlights as item}
				<div
					class="sticker relative h-64 w-64 bg-brand-purple p-6 flex flex-col justify-center items-center text-center transition-transform hover:scale-110 hover:z-10"
				>
					<span
						class="absolute top-4 right-4 rotate-12 bg-brand-red px-2 py-1 font-anton text-sm text-white shadow-sm"
					>
						{item.tag}
					</span>
					<h3 class="font-anton text-3xl text-white leading-tight">
						{item.title}
					</h3>
					<button
						class="mt-4 font-montserrat text-sm font-bold text-brand-yellow underline decoration-2 underline-offset-2"
					>
						Saiba mais
					</button>
				</div>
			{/each}
		</div>
	</div>
</section>
