<script>
	import { fly } from 'svelte/transition';
	import CustomPackagesSection from '$lib/components/CustomPackagesSection.svelte';
	import StickerButton from '$lib/components/StickerButton.svelte';
	import MessageCircle from 'lucide-svelte/icons/message-circle';

	let individualPackages = [
		{
			hours: '1h semanal',
			semesterPrice: 'R$370,00',
			annualPrice: 'R$341,00'
		},
		{
			hours: '1h30 semanal',
			semesterPrice: 'R$518,00',
			annualPrice: 'R$481,00'
		},
		{
			hours: '2h semanais',
			semesterPrice: 'R$665,00',
			annualPrice: 'R$608,00'
		}
	];

	let groupPackages = [
		{
			hours: '1h semanal',
			semesterPrice: 'R$220,00',
			annualPrice: 'R$200,00'
		},
		{
			hours: '1h30 semanal',
			semesterPrice: 'R$331,00',
			annualPrice: 'R$300,00'
		},
		{
			hours: '2h semanais',
			semesterPrice: 'R$441,00',
			annualPrice: 'R$400,00'
		}
	];

	function getWhatsAppLink(pkg, type, period) {
		const price = period === 'Semestral' ? pkg.semesterPrice : pkg.annualPrice;
		const message = `Olá! Tenho interesse no pacote ${type} de ${pkg.hours} (${period}) por ${price}. Gostaria de mais informações.`;
		return `https://wa.me/559293120574?text=${encodeURIComponent(message)}`;
	}
</script>

<div class="min-h-screen font-body">
	<!-- INDIVIDUAL PACKAGES SECTION -->
	<section
		class="relative overflow-hidden bg-brand-purple px-6 py-12 text-center md:px-12 md:py-20"
	>
		<!-- Header -->
		<div class="mb-12">
			<div
				class="inline-block -rotate-2 transform bg-brand-yellow px-8 py-4 shadow-[8px_8px_0px_rgba(0,0,0,0.3)]"
			>
				<h1 class="font-display text-5xl uppercase text-brand-purple md:text-7xl">
					Pacotes Individuais
				</h1>
			</div>
			<p class="mx-auto mt-8 max-w-4xl text-xl font-bold text-brand-yellow md:text-2xl">
				Aulas online, ao vivo e privadas. Só você, seu professor(a) e aulas exclusivamente
				preparadas para o seus objetivos!
			</p>
		</div>

		<!-- Semestral -->
		<div class="mb-16">
			<h2
				class="mb-2 font-display text-4xl uppercase text-brand-yellow underline decoration-4 underline-offset-8 md:text-5xl"
			>
				Pacotes Semestrais
			</h2>
			<p class="mb-8 text-xl font-bold italic text-brand-yellow">25 semanas</p>

			<div class="grid gap-8 md:grid-cols-3">
				{#each individualPackages as pkg, i}
					<div
						class="group relative flex flex-col items-center justify-between rounded-3xl border-4 border-brand-yellow bg-brand-yellow p-6 text-brand-purple shadow-[8px_8px_0px_rgba(0,0,0,0.3)] transition-all duration-300 hover:scale-105"
						in:fly={{ y: 50, duration: 800, delay: i * 200 }}
					>
						<div>
							<h3
								class="mb-4 rounded-full bg-brand-purple py-2 font-display text-2xl text-brand-yellow"
							>
								{pkg.hours}
							</h3>
							<p class="text-lg font-bold">6 mensalidades de</p>
							<p class="font-display text-5xl italic">{pkg.semesterPrice}</p>
						</div>

						<!-- Button: Always visible on mobile, expands on hover on desktop -->
						<div
							class="mt-6 w-full md:max-h-0 md:overflow-hidden md:transition-all md:duration-300 md:group-hover:max-h-32"
						>
							<div class="flex justify-center pt-2 pb-4">
								<StickerButton
									text="EU QUERO"
									color="purple"
									icon={MessageCircle}
									link={getWhatsAppLink(pkg, 'Individual', 'Semestral')}
								/>
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>

		<!-- Anual -->
		<div>
			<h2
				class="mb-2 font-display text-4xl uppercase text-brand-yellow underline decoration-4 underline-offset-8 md:text-5xl"
			>
				Pacotes Anuais
			</h2>
			<p class="mb-8 text-xl font-bold italic text-brand-yellow">50 semanas</p>

			<div class="grid gap-8 md:grid-cols-3">
				{#each individualPackages as pkg, i}
					<div
						class="group relative flex flex-col items-center justify-between rounded-3xl border-4 border-brand-yellow bg-brand-purple p-6 text-brand-yellow shadow-[8px_8px_0px_rgba(255,255,0,0.3)] transition-all duration-300 hover:scale-105"
						in:fly={{ y: 50, duration: 800, delay: (i + 3) * 200 }}
					>
						<div>
							<h3
								class="mb-4 rounded-full bg-brand-yellow py-2 font-display text-2xl text-brand-purple"
							>
								{pkg.hours}
							</h3>
							<p class="text-lg font-bold">12 mensalidades de</p>
							<p class="font-display text-5xl italic">{pkg.annualPrice}</p>
						</div>

						<div
							class="mt-6 w-full md:max-h-0 md:overflow-hidden md:transition-all md:duration-300 md:group-hover:max-h-32"
						>
							<div class="flex justify-center pt-2 pb-4">
								<StickerButton
									text="EU QUERO"
									color="yellow"
									icon={MessageCircle}
									link={getWhatsAppLink(pkg, 'Individual', 'Anual')}
								/>
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- GROUP PACKAGES SECTION -->
	<section
		class="relative overflow-hidden border-t-4 border-brand-brown bg-brand-cream px-6 py-12 text-center md:px-12 md:py-20"
	>
		<!-- Header -->
		<div class="mb-12">
			<div
				class="inline-block rotate-1 transform bg-brand-brown px-8 py-4 shadow-[8px_8px_0px_rgba(0,0,0,0.2)]"
			>
				<h1 class="font-display text-4xl uppercase text-white md:text-6xl">
					Turmas a partir de 4 pessoas
				</h1>
			</div>
			<p class="mx-auto mt-8 max-w-4xl text-xl font-bold text-brand-brown md:text-2xl">
				Aulas online, ao vivo e grupais. Você aprende com outras pessoas, podendo trazer junto
				consigo amigos ou colegas!
			</p>
		</div>

		<!-- Semestral -->
		<div class="mb-16">
			<h2
				class="mb-2 font-display text-4xl uppercase text-brand-brown underline decoration-4 underline-offset-8 md:text-5xl"
			>
				Pacotes Semestrais
			</h2>
			<p class="mb-8 text-xl font-bold italic text-brand-brown">25 semanas</p>

			<div class="grid gap-8 md:grid-cols-3">
				{#each groupPackages as pkg, i}
					<div
						class="group relative flex flex-col items-center justify-between rounded-3xl border-4 border-brand-brown bg-white p-6 text-brand-brown shadow-[8px_8px_0px_rgba(88,28,12,0.3)] transition-all duration-300 hover:scale-105"
						in:fly={{ y: 50, duration: 800, delay: i * 200 }}
					>
						<div>
							<h3 class="mb-4 rounded-lg bg-brand-brown py-2 font-display text-2xl text-white">
								{pkg.hours}
							</h3>
							<p class="text-lg font-bold">6 mensalidades de</p>
							<p class="font-display text-5xl italic">{pkg.semesterPrice}</p>
						</div>

						<div
							class="mt-6 w-full md:max-h-0 md:overflow-hidden md:transition-all md:duration-300 md:group-hover:max-h-32"
						>
							<div class="flex justify-center pt-2 pb-4">
								<StickerButton
									text="EU QUERO"
									color="brown"
									icon={MessageCircle}
									link={getWhatsAppLink(pkg, 'Grupo', 'Semestral')}
								/>
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>

		<!-- Anual -->
		<div>
			<h2
				class="mb-2 font-display text-4xl uppercase text-brand-brown underline decoration-4 underline-offset-8 md:text-5xl"
			>
				Pacotes Anuais
			</h2>
			<p class="mb-8 text-xl font-bold italic text-brand-brown">50 semanas</p>

			<div class="grid gap-8 md:grid-cols-3">
				{#each groupPackages as pkg, i}
					<div
						class="group relative flex flex-col items-center justify-between rounded-3xl border-4 border-brand-brown bg-brand-brown p-6 text-white shadow-[8px_8px_0px_rgba(0,0,0,0.3)] transition-all duration-300 hover:scale-105"
						in:fly={{ y: 50, duration: 800, delay: (i + 3) * 200 }}
					>
						<div>
							<h3 class="mb-4 rounded-lg bg-white py-2 font-display text-2xl text-brand-brown">
								{pkg.hours}
							</h3>
							<p class="text-lg font-bold">12 mensalidades de</p>
							<p class="font-display text-5xl italic">{pkg.annualPrice}</p>
						</div>

						<div
							class="mt-6 w-full md:max-h-0 md:overflow-hidden md:transition-all md:duration-300 md:group-hover:max-h-32"
						>
							<div class="flex justify-center pt-2 pb-4">
								<StickerButton
									text="EU QUERO"
									color="white"
									icon={MessageCircle}
									link={getWhatsAppLink(pkg, 'Grupo', 'Anual')}
								/>
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</section>

	<!-- CUSTOM PACKAGES SECTION -->
	<CustomPackagesSection />
</div>
