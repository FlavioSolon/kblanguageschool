<script>
	/** @type {{ text: string, link?: string, color?: 'red' | 'purple' | 'pink' | 'yellow' | 'orange' | 'white', icon?: any }} */
	let { text, link = '#', color = 'red', icon: Icon } = $props();

	const colorClasses = {
		red: 'bg-brand-red text-white',
		purple: 'bg-brand-purple text-white',
		pink: 'bg-brand-pink text-brand-brown',
		yellow: 'bg-brand-yellow text-brand-brown',
		orange: 'bg-brand-orange text-white',
		white: 'bg-white text-brand-orange'
	};

	let selectedColor = $derived(colorClasses[color] || colorClasses.red);
</script>

<a
	href={link}
	class="inline-flex items-center gap-2 rounded-full border-2 border-brand-brown px-6 py-3 font-display text-xl uppercase tracking-wide shadow-[4px_4px_0px_black] transition-all hover:scale-105 active:translate-x-[2px] active:translate-y-[2px] active:shadow-[2px_2px_0px_black] {selectedColor}"
>
	{#if Icon}
		<span class="text-lg">
			<Icon />
		</span>
	{/if}
	{text}
</a>
