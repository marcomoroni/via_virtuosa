<script lang="ts">
	import PageLinkArrow from './PageLinkArrow.svelte';

	let { href, label }: { href: string; label: string } = $props();
</script>

<a class="font-color-accent font-line-height-default" {href}
	>{label}<span class="arrow"><PageLinkArrow /></span></a
>

<style>
	.arrow {
		margin-inline-start: 12px;
		position: relative;
		top: 0.2px;
	}
</style>
