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
				href="https://www.instagram.com/kblanguageschool?igsh=MXhqeWQ3ZGlleXIwZQ%3D%3D"
				target="_blank"
				class="flex h-12 w-12 items-center justify-center border-2 border-brand-brown bg-white shadow-[4px_4px_0px_rgba(88,28,12,1)] transition-transform hover:-translate-y-1 hover:shadow-[6px_6px_0px_rgba(88,28,12,1)]"
			>
				<Instagram size={24} />
			</a>
			<a
				href="https://wa.me/559293120574?text=Ol%C3%A1!%20Tenho%20interesse%20nas%20aulas%20e%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es."
				target="_blank"
				class="flex h-12 w-12 items-center justify-center border-2 border-brand-brown bg-white shadow-[4px_4px_0px_rgba(88,28,12,1)] transition-transform hover:-translate-y-1 hover:shadow-[6px_6px_0px_rgba(88,28,12,1)]"
			>
				<MessageCircle size={24} />
			</a>
		</div>

		<div class="font-pacifico text-lg text-white">
			© {new Date().getFullYear()} KB School
		</div>
	</div>
</footer>
