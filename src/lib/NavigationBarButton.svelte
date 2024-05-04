<script lang="ts">
	let { label, highlight }: { label: string; highlight: boolean } = $props();
</script>

<button class="font-size-default font-weight-default font-color-accent-dark" class:highlight>
	{label}
</button>

<style>
	button {
		--horizontal-padding: 26px;
		--vertical-padding: 19px;
		padding-left: var(--horizontal-padding);
		padding-right: var(--horizontal-padding);
		padding-top: var(--vertical-padding);
		padding-bottom: var(--vertical-padding);
		text-wrap: nowrap;
		display: grid;
		border-radius: calc(infinity * 1px);
		border: 2px solid #dad5cf;
		transition:
			border-color 1.5s ease-in-out,
			var(--border-radius-transition);
	}

	.highlight {
		border-color: var(--color-accent-dark);
		border-top-left-radius: 0;
		border-bottom-left-radius: 0;
	}
</style>
