<script>
	import { fly } from 'svelte/transition';

	const cards = [
		{
			title: 'MISSÃO',
			text: 'Ensinar idiomas de forma acessível, personalizada e prática, respeitando o ritmo e os objetivos de cada aluno. Nosso foco é ajudar brasileiros a conquistarem mais oportunidades pessoais e profissionais por meio do domínio de línguas estrangeiras.'
		},
		{
			title: 'VISÃO',
			text: 'Ser reconhecida como uma escola de idiomas online referência em atendimento humanizado, resultados reais e ensino de qualidade. Em cinco anos, queremos expandir nossa base de alunos e oferecer programas diversificados, mantendo sempre o cuidado individual com cada um.'
		}
	];

	const values = [
		'Respeito à individualidade de cada aluno.',
		'Clareza e honestidade na comunicação.',
		'Comprometimento com o aprendizado real.',
		'Empatia no atendimento e nas relações.',
		'Evolução contínua.'
	];
</script>

<section id="quem-somos" class="relative bg-brand-pink px-6 py-20 border-t-4 border-brand-brown">
	<!-- Yellow Scribbles Border Decoration (CSS approximation) -->
	<div
		class="absolute top-0 left-0 w-full h-4 bg-brand-yellow"
		style="clip-path: polygon(0% 0%, 5% 100%, 10% 0%, 15% 100%, 20% 0%, 25% 100%, 30% 0%, 35% 100%, 40% 0%, 45% 100%, 50% 0%, 55% 100%, 60% 0%, 65% 100%, 70% 0%, 75% 100%, 80% 0%, 85% 100%, 90% 0%, 95% 100%, 100% 0%);"
	></div>

	<div class="mx-auto max-w-7xl">
		<div class="mb-16 text-center">
			<h2
				class="inline-block bg-white px-8 py-2 font-display text-5xl text-brand-brown border-4 border-brand-brown shadow-[6px_6px_0px_rgba(0,0,0,1)] -rotate-2"
			>
				QUEM SOMOS?
			</h2>
		</div>

		<div class="grid gap-8 md:grid-cols-3">
			<!-- Missão & Visão -->
			{#each cards as card, i}
				<div
					in:fly={{ y: 50, duration: 800, delay: i * 200 }}
					class="flex flex-col rounded-3xl border-4 border-brand-brown p-8 hover:bg-white/10 transition-colors"
				>
					<h3
						class="mb-6 text-center font-display text-3xl text-brand-yellow drop-shadow-[2px_2px_0px_black]"
					>
						{card.title}
					</h3>
					<p class="font-body text-lg font-bold text-brand-brown leading-relaxed">
						{card.text}
					</p>
				</div>
			{/each}

			<!-- Valores -->
			<div
				in:fly={{ y: 50, duration: 800, delay: 400 }}
				class="flex flex-col rounded-3xl border-4 border-brand-brown p-8 hover:bg-white/10 transition-colors"
			>
				<h3
					class="mb-6 text-center font-display text-3xl text-brand-yellow drop-shadow-[2px_2px_0px_black]"
				>
					VALORES
				</h3>
				<ul
					class="list-disc pl-5 font-body text-lg font-bold text-brand-brown leading-relaxed space-y-2 marker:text-brand-yellow"
				>
					{#each values as value}
						<li>{value}</li>
					{/each}
				</ul>
			</div>
		</div>
	</div>
</section>
