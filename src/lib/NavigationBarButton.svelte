<script lang="ts">
	let { label, highlight }: { label: string; highlight: boolean } = $props();
</script>

<button class="font-size-default font-weight-default font-color-accent-dark" class:highlight>
	<div class="label font-size-default font-weight-default font-color-accent-dark">
		{label}
	</div>
</button>

<style>
	button {
		--horizontal-padding: 22px;
		padding-left: var(--horizontal-padding);
		padding-right: var(--horizontal-padding);
		height: 52px;
		display: grid;
		border-radius: calc(infinity * 1px);
		border: 2px solid #dad5cf;
		transition:
			border-color 1.5s ease-in-out,
			var(--border-radius-transition);
	}

	.label {
		text-wrap: nowrap;
		align-self: center;
		justify-self: center;
	}

	.highlight {
		border-color: var(--color-accent-dark);
		border-top-left-radius: 0;
		border-bottom-left-radius: 0;
	}
</style>
