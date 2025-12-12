<script>
	/** @type {{ color?: string }} */
	let { color = 'brand-purple' } = $props();
</script>

<div
	class="pointer-events-none absolute inset-0 opacity-10"
	style="background-image: radial-gradient(var(--color-{color}) 1px, transparent 1px); background-size: 10px 10px;"
></div>
