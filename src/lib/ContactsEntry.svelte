<script lang="ts">
	import type { Snippet } from 'svelte';

	let { icon, text, href }: { icon: Snippet; text: Snippet; href: string | undefined } = $props();
</script>

<li class="entry">
	<a {href}>
		<div class="icon">
			{@render icon()}
		</div>
		<div class="text font-color-light font-line-height-default font-weight-default">
			{@render text()}
		</div>
	</a>
</li>

<style>
	.entry {
		background-color: #f1efec;
	}

	a {
		display: grid;
		grid-template-columns: min-content 1fr;
		column-gap: 20px;
		padding: 25px;
	}

	.icon {
		grid-column: 1 / 2;
		align-self: center;
	}

	.icon :global(*) {
		stroke: var(--color-base-light);
	}

	.text {
		grid-column: 2 / 3;
		align-self: center;
	}
</style>
