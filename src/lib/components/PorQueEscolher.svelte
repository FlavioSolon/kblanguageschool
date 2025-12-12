<script>
	const reasons = [
		{ title: 'Metodologia Ativa', desc: 'Nada de ficar só copiando do quadro. Aqui você fala!' },
		{ title: 'Material Exclusivo', desc: 'Conteúdo criado pensando em você e no mundo real.' },
		{ title: 'Aulas Flexíveis', desc: 'Online ou presencial, no seu ritmo.' }
	];
</script>

<section id="por-que-escolher" class="bg-brand-red px-6 py-20 border-t-4 border-brand-brown">
	<div class="mx-auto max-w-6xl text-center">
		<h2
			class="font-anton mb-12 text-4xl uppercase text-brand-yellow drop-shadow-[3px_3px_0px_rgba(66,28,28,1)] md:text-6xl"
		>
			Por Que Escolher?
		</h2>

		<div class="grid gap-8 md:grid-cols-3">
			{#each reasons as reason, i}
				<div
					class="hard-shadow group bg-brand-cream p-6 text-left border-2 border-brand-brown transition-transform hover:-translate-y-2 hover:rotate-1"
				>
					<div class="font-anton mb-4 text-5xl text-brand-purple opacity-20">0{i + 1}</div>
					<h3 class="font-anton mb-2 text-2xl text-brand-brown">{reason.title}</h3>
					<p class="font-montserrat font-medium text-brand-brown">{reason.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
