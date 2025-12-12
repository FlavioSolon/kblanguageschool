<script>
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let visible = $state(false);

	onMount(() => {
		visible = true;
	});
</script>

<section class="relative min-h-[600px] overflow-hidden bg-brand-purple px-6 py-20 text-center">
	<!-- Spiral Background (CSS Radial Gradient approximation for spirals) -->
	<div
		class="absolute inset-0 opacity-30 pointer-events-none"
		style="background: radial-gradient(circle at center, transparent 0%, transparent 20%, #4a1d6e 20%, #4a1d6e 22%, transparent 22%, transparent 40%, #4a1d6e 40%, #4a1d6e 42%, transparent 42%, transparent 60%, #4a1d6e 60%, #4a1d6e 62%, transparent 62%, transparent 80%, #4a1d6e 80%, #4a1d6e 82%, transparent 82%); background-size: 200px 200px;"
	></div>

	<div class="relative z-10 mx-auto flex h-full max-w-7xl items-center justify-center">
		<!-- Center Text -->
		<div class="flex flex-col items-center justify-center z-20">
			<h1
				class="font-display text-8xl md:text-9xl text-white drop-shadow-[6px_6px_0px_rgba(0,0,0,1)] tracking-tighter"
			>
				WELCOME!
			</h1>
			<div
				class="mt-4 -rotate-2 bg-brand-yellow px-8 py-2 border-4 border-black shadow-[4px_4px_0px_rgba(0,0,0,1)]"
			>
				<span class="font-hand text-3xl md:text-5xl text-brand-brown font-bold">
					to our school
				</span>
			</div>
		</div>
	</div>
</section>
