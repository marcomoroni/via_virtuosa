<script lang="ts">
	import PageLinkArrow from './PageLinkArrow.svelte';

	let {
		href,
		label,
		color = 'accent'
	}: { href: string; label: string; color?: 'accent' | 'blue' } = $props();
</script>

<a
	class="font-line-height-default"
	class:font-color-accent={color === 'accent'}
	class:blue={color === 'blue'}
	{href}>{label}<span class="arrow"><PageLinkArrow {color} /></span></a
>

<style>
	.arrow {
		margin-inline-start: 12px;
		position: relative;
		top: 0.2px;
	}

	.arrow :global(svg) {
		display: inline-block;
	}

	a.blue {
		color: var(--color-csa-blue);
	}
</style>
