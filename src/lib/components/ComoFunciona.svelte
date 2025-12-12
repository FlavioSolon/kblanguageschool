<script>
	import { fly } from 'svelte/transition';

	let steps = [
		{ number: 1, text: 'Agende sua aula experimental' },
		{ number: 2, text: 'Converse com um professor ao vivo' },
		{ number: 3, text: 'Escolha seu plano ideal' },
		{ number: 4, text: 'Pratique toda semana e evolua com a gente' }
	];
</script>

<section class="relative overflow-hidden bg-brand-purple py-20">
	<!-- Footprint Decoration Background (Static positions to avoid hydration mismatch) -->
	<div class="absolute inset-0 opacity-10 pointer-events-none">
		<div class="absolute top-[10%] left-[5%] text-brand-yellow rotate-12 text-4xl">👣</div>
		<div class="absolute top-[30%] left-[80%] text-brand-yellow -rotate-12 text-4xl">👣</div>
		<div class="absolute top-[60%] left-[15%] text-brand-yellow rotate-45 text-4xl">👣</div>
		<div class="absolute top-[80%] left-[70%] text-brand-yellow -rotate-6 text-4xl">👣</div>
		<div class="absolute top-[20%] left-[40%] text-brand-yellow rotate-90 text-4xl">👣</div>
		<div class="absolute top-[50%] left-[90%] text-brand-yellow -rotate-45 text-4xl">👣</div>
	</div>

	<div class="relative mx-auto max-w-6xl px-6">
		<h2
			class="mb-16 text-center font-display text-6xl text-white drop-shadow-[4px_4px_0px_rgba(0,0,0,0.5)] md:text-8xl"
			in:fly={{ y: -50, duration: 800 }}
		>
			Como Funciona?
		</h2>

		<div class="grid gap-12 md:grid-cols-2">
			<!-- Steps List -->
			<div class="flex flex-col justify-center gap-8">
				{#each steps as step, i}
					<div class="flex items-center gap-6" in:fly={{ x: -50, duration: 800, delay: i * 200 }}>
						<div
							class="flex h-16 w-16 flex-shrink-0 items-center justify-center rounded-full border-4 border-white bg-brand-orange shadow-[4px_4px_0px_rgba(0,0,0,0.3)]"
						>
							<span class="font-display text-4xl text-white">{step.number}</span>
						</div>
						<p class="font-display text-2xl text-white md:text-3xl">
							{step.text}
						</p>
					</div>
				{/each}
			</div>

			<!-- Footprints Decoration (CSS Art or SVG placeholder) -->
			<div class="relative hidden min-h-[400px] md:block">
				<!-- Footprint 1 -->
				<div
					class="absolute right-[20%] top-[10%] rotate-[15deg] text-brand-yellow opacity-80"
					in:fly={{ y: 50, duration: 800, delay: 200 }}
				>
					<svg width="80" height="120" viewBox="0 0 100 150" fill="currentColor">
						<path
							d="M30,10 C10,30 0,60 10,90 C20,120 50,140 70,130 C90,120 100,90 90,60 C80,30 50,0 30,10 Z M20,135 C10,135 5,125 10,120 C15,115 25,120 30,125 C35,130 30,140 20,135 Z"
						/>
					</svg>
				</div>
				<!-- Footprint 2 -->
				<div
					class="absolute right-[40%] top-[30%] rotate-[-10deg] text-brand-yellow opacity-80"
					in:fly={{ y: 50, duration: 800, delay: 400 }}
				>
					<svg width="80" height="120" viewBox="0 0 100 150" fill="currentColor">
						<path
							d="M30,10 C10,30 0,60 10,90 C20,120 50,140 70,130 C90,120 100,90 90,60 C80,30 50,0 30,10 Z M20,135 C10,135 5,125 10,120 C15,115 25,120 30,125 C35,130 30,140 20,135 Z"
						/>
					</svg>
				</div>
				<!-- Footprint 3 -->
				<div
					class="absolute right-[25%] top-[55%] rotate-[20deg] text-brand-yellow opacity-80"
					in:fly={{ y: 50, duration: 800, delay: 600 }}
				>
					<svg width="80" height="120" viewBox="0 0 100 150" fill="currentColor">
						<path
							d="M30,10 C10,30 0,60 10,90 C20,120 50,140 70,130 C90,120 100,90 90,60 C80,30 50,0 30,10 Z M20,135 C10,135 5,125 10,120 C15,115 25,120 30,125 C35,130 30,140 20,135 Z"
						/>
					</svg>
				</div>
				<!-- Footprint 4 -->
				<div
					class="absolute right-[45%] top-[75%] rotate-[-5deg] text-brand-yellow opacity-80"
					in:fly={{ y: 50, duration: 800, delay: 800 }}
				>
					<svg width="80" height="120" viewBox="0 0 100 150" fill="currentColor">
						<path
							d="M30,10 C10,30 0,60 10,90 C20,120 50,140 70,130 C90,120 100,90 90,60 C80,30 50,0 30,10 Z M20,135 C10,135 5,125 10,120 C15,115 25,120 30,125 C35,130 30,140 20,135 Z"
						/>
					</svg>
				</div>
			</div>
		</div>
	</div>
</section>
