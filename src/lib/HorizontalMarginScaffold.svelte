<script lang="ts">
	import type { Snippet } from 'svelte';

	let { children }: { children: Snippet } = $props();
</script>

<div class="scaffold">
	<div class="margin left"></div>
	<div class="content">
		{@render children()}
	</div>
	<div class="margin right"></div>
</div>

<style>
	.scaffold {
		display: grid;
		grid-template-columns: 100px 1fr 100px;
	}

	.left,
	.content,
	.right {
		grid-row: 1 / 2;
	}

	.left {
		grid-column: 1 / 2;
	}

	.content {
		grid-column: 2 / 3;
	}

	.right {
		grid-column: 3 / 4;
	}

	@media (min-width: 1800px) {
		.scaffold {
			grid-template-columns: 1fr 1600px 1fr;
		}
	}

	@media (max-width: 800px) {
		.scaffold {
			grid-template-columns: 1fr 600px 1fr;
		}
	}

	@media (max-width: 660px) {
		.scaffold {
			grid-template-columns: 30px 1fr 30px;
		}
	}
</style>
