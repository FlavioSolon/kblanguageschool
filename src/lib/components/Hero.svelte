<script>
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let visible = $state(false);

	onMount(() => {
		visible = true;
	});
</script>

<section class="relative min-h-[600px] overflow-hidden bg-brand-purple px-6 py-20 text-center">
	<!-- Spiral Background -->
	<div
		class="absolute inset-0 opacity-30 pointer-events-none"
		style="background: radial-gradient(circle at center, transparent 0%, transparent 20%, #4a1d6e 20%, #4a1d6e 22%, transparent 22%, transparent 40%, #4a1d6e 40%, #4a1d6e 42%, transparent 42%, transparent 60%, #4a1d6e 60%, #4a1d6e 62%, transparent 62%, transparent 80%, #4a1d6e 80%, #4a1d6e 82%, transparent 82%); background-size: 200px 200px;"
	></div>

	{#if visible}
		<!-- Keity Confiante - Mobile (menor e à frente do texto) -->
		<div
			in:fly={{ y: 50, duration: 800, delay: 300 }}
			class="absolute left-2 bottom-0 w-[280px] h-[360px] md:hidden bg-cover bg-bottom bg-no-repeat z-10"
			style="background-image: url('/keity_confiante.png');"
		></div>

		<!-- Keity Confiante - Desktop (esquerda, encostando na borda inferior) -->
		<div
			in:fly={{ y: 50, duration: 800, delay: 300 }}
			class="absolute left-0 bottom-[-26px] w-[380px] h-[620px] hidden md:block bg-cover bg-bottom bg-no-repeat z-10"
			style="background-image: url('/keity_confiante.png');"
		></div>

		<!-- Keity Sorrindo - Desktop (direita, rosto completo, maior altura) -->
		<div
			in:fly={{ y: 50, duration: 800, delay: 500 }}
			class="absolute right-0 bottom-[-10px] w-[600px] h-[620px] hidden md:block bg-cover bg-center bg-no-repeat z-10"
			style="background-image: url('/keity_sorrindo.png');"
		></div>
	{/if}

	<div class="relative z-20 mx-auto flex h-full max-w-7xl items-center justify-center">
		<!-- Center Text (z-20 para ficar na frente das imagens) -->
		<div class="flex flex-col items-center justify-center">
			{#if visible}
				<h1
					in:fly={{ y: -50, duration: 800 }}
					class="font-display text-8xl md:text-9xl text-white drop-shadow-[6px_6px_0px_rgba(0,0,0,1)] tracking-tighter"
				>
					WELCOME!
				</h1>
				<div
					in:fly={{ y: 50, duration: 800, delay: 200 }}
					class="mt-4 -rotate-2 bg-brand-yellow px-8 py-2 border-4 border-black shadow-[4px_4px_0px_rgba(0,0,0,1)]"
				>
					<span class="font-hand text-3xl md:text-5xl text-brand-brown font-bold">
						to our school
					</span>
				</div>
			{/if}
		</div>
	</div>
</section>
