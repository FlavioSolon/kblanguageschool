<script>
	import { fly } from 'svelte/transition';
	import StickerButton from './StickerButton.svelte';
	import MessageCircle from 'lucide-svelte/icons/message-circle';
</script>

<section class="relative overflow-hidden border-t-4 border-brand-brown">
	<!-- Top Half: Yellow -->
	<div class="bg-brand-yellow px-6 py-16 text-center md:px-12 md:py-20">
		<h2
			class="font-display text-5xl uppercase leading-none text-brand-orange drop-shadow-[4px_4px_0px_rgba(0,0,0,0.2)] md:text-7xl"
			in:fly={{ y: 50, duration: 800 }}
		>
			Pacotes Personalizados
		</h2>
		<p
			class="mx-auto mt-6 max-w-3xl font-body text-xl font-bold text-brand-orange md:text-2xl"
			in:fly={{ y: 50, duration: 800, delay: 200 }}
		>
			Precisa de uma carga horária semanal maior? Fazer aulas por um período mais curto de tempo?
			Solicite um orçamento conosco!
		</p>
	</div>

	<!-- Bottom Half: Orange -->
	<div class="relative bg-brand-orange px-6 py-12 text-center md:px-12 md:py-16">
		<div class="flex flex-col items-center justify-center gap-8 md:flex-row md:gap-16">
			<!-- Megaphone Image Placeholder -->
			<div
				class="relative h-48 w-48 md:h-64 md:w-64"
				in:fly={{ x: -50, duration: 800, delay: 400 }}
			>
				<!-- Replace with actual megaphone image -->
				<div
					class="absolute inset-0 rotate-[-15deg] transform rounded-full border-4 border-black bg-white shadow-[8px_8px_0px_black]"
				>
					<div class="flex h-full items-center justify-center font-display text-4xl text-black">
						📢
					</div>
				</div>
			</div>

			<!-- CTA Button -->
			<div in:fly={{ x: 50, duration: 800, delay: 400 }}>
				<StickerButton
					text="FALE COM A GENTE"
					link="https://wa.me/5511999999999"
					color="yellow"
					icon={MessageCircle}
				/>
			</div>

			<!-- Phone/Hand Image Placeholder -->
			<div
				class="relative hidden h-48 w-48 md:block md:h-64 md:w-64"
				in:fly={{ x: 50, duration: 800, delay: 600 }}
			>
				<!-- Replace with actual hand/phone image -->
				<div
					class="absolute inset-0 rotate-[15deg] transform rounded-full border-4 border-black bg-white shadow-[8px_8px_0px_black]"
				>
					<div class="flex h-full items-center justify-center font-display text-4xl text-black">
						📱
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
