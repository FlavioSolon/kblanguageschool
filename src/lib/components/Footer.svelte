<script>
	import { Instagram, Mail, MessageCircle } from 'lucide-svelte';
</script>

<footer class="border-t-4 border-brand-brown bg-brand-orange px-6 py-12 text-brand-brown">
	<div class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-6 md:flex-row">
		<div class="text-center md:text-left">
			<h2 class="font-anton text-2xl text-white drop-shadow-[2px_2px_0px_rgba(0,0,0,1)]">
				KB LANGUAGE SCHOOL
			</h2>
			<p class="font-montserrat mt-2 font-bold">Aprenda idiomas com estilo.</p>
		</div>

		<div class="flex gap-4">
			<a
				href="https://instagram.com"
				target="_blank"
				rel="noopener noreferrer"
				class="bg-white p-3 border-2 border-brand-brown hard-shadow hover:-translate-y-1 transition-transform"
				aria-label="Instagram"
			>
				<Instagram size={24} />
			</a>
			<a
				href="mailto:info@kbschool.com"
				target="_blank"
				rel="noopener noreferrer"
				class="bg-white p-3 border-2 border-brand-brown hard-shadow hover:-translate-y-1 transition-transform"
				aria-label="Email"
			>
				<Mail size={24} />
			</a>
			<a
				href="https://wa.me/5511999999999"
				target="_blank"
				rel="noopener noreferrer"
				class="bg-white p-3 border-2 border-brand-brown hard-shadow hover:-translate-y-1 transition-transform"
				aria-label="WhatsApp"
			>
				<MessageCircle size={24} />
			</a>
		</div>

		<div class="font-pacifico text-lg text-white">
			© {new Date().getFullYear()} KB School
		</div>
	</div>
</footer>
