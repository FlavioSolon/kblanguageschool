<script>
	const steps = [
		'Agende sua aula experimental',
		'Converse com professor',
		'Escolha seu plano',
		'Pratique toda semana'
	];
</script>

<section
	id="como-funciona"
	class="relative overflow-hidden bg-brand-purple px-6 py-20 border-t-4 border-brand-brown"
>
	<!-- Footprints Decoration (CSS approximation) -->
	<div
		class="absolute top-1/2 left-0 w-full h-20 pointer-events-none opacity-20 flex justify-between px-10"
	>
		<div class="w-12 h-20 bg-brand-yellow rounded-full rotate-45"></div>
		<div class="w-12 h-20 bg-brand-yellow rounded-full -rotate-45 mt-10"></div>
		<div class="w-12 h-20 bg-brand-yellow rounded-full rotate-45"></div>
		<div class="w-12 h-20 bg-brand-yellow rounded-full -rotate-45 mt-10"></div>
		<div class="w-12 h-20 bg-brand-yellow rounded-full rotate-45"></div>
		<div class="w-12 h-20 bg-brand-yellow rounded-full -rotate-45 mt-10"></div>
	</div>

	<div class="relative z-10 mx-auto max-w-6xl">
		<h2
			class="font-hand mb-16 text-center text-5xl text-white drop-shadow-[4px_4px_0px_black] md:text-7xl"
		>
			Como Funciona?
		</h2>

		<div class="grid gap-8 md:grid-cols-4">
			{#each steps as step, i}
				<div class="flex flex-col items-center text-center group">
					<div
						class="mb-6 flex h-24 w-24 items-center justify-center rounded-full bg-brand-yellow border-4 border-black shadow-[4px_4px_0px_black] transition-transform group-hover:scale-110 group-hover:rotate-6"
					>
						<span class="font-display text-5xl text-brand-brown">{i + 1}</span>
					</div>
					<p class="font-display text-2xl text-white leading-tight max-w-[200px]">
						{step}
					</p>
				</div>
			{/each}
		</div>
	</div>
</section>
