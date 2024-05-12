<script lang="ts">
	import type { Snippet } from 'svelte';

	let {
		illustration,
		illustrationBackgroundColor,
		header,
		text,
		link,
		background
	}: {
		illustration: Snippet;
		illustrationBackgroundColor?: string;
		header: Snippet;
		text: string;
		link: Snippet;
		background?: 'blue';
	} = $props();
</script>

<div class="grid" class:background-blue={background === 'blue'}>
	<div class="image-background" style:background-color={illustrationBackgroundColor}></div>
	<div class="image-container">
		{@render illustration()}
	</div>
	<div class="type" class:with-padding={background !== undefined}>
		<h2 class="font-color-dark font-weight-default" class:white={background === 'blue'}>
			{@render header()}
		</h2>
		<div class="title-gap"></div>
		<p
			class="font-color-light font-line-height-default font-weight-default"
			class:white={background === 'blue'}
		>
			{text}
		</p>
		<div class="small-gap"></div>
		{@render link()}
	</div>
</div>

<style>
	.grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
	}

	.background-blue {
		background-color: #72c1ee;
	}

	.image-container {
		grid-row: 1 / 2;
		grid-column: 1 / 2;
		align-self: center;
		aspect-ratio: 1 / 1;
	}

	.image-background {
		grid-row: 1 / 2;
		grid-column: 1 / 2;
		align-self: stretch;
		justify-self: stretch;
	}

	.type {
		grid-row: 1 / 2;
		grid-column: 2 / 3;
		padding-left: 70px;
		padding-right: 70px;
		align-self: center;
		max-width: 540px;
	}

	.type.with-padding {
		padding-top: 50px;
		padding-bottom: 50px;
	}

	@media (max-width: 1300px) {
		.type {
			padding-left: 50px;
			padding-right: 50px;
		}
	}

	@media (max-width: 1000px) {
		.grid {
			display: grid;
			grid-template-columns: unset;
			column-gap: unset;
			row-gap: 50px;
		}

		.image-container,
		.image-background {
			grid-column: 1 / 2;
			grid-row: 1 / 2;
		}

		.type {
			grid-column: 1 / 2;
			grid-row: 2 / 3;
			padding-left: unset;
			padding-right: unset;
		}

		.type.with-padding {
			padding-top: unset;
			padding-left: 50px;
			padding-right: 50px;
			padding-bottom: 50px;
		}
	}

	h2 {
		font-size: 40px;
		line-height: 1.4;
		text-wrap: balance;
	}

	h2.white {
		color: #ffffff8f;
	}

	h2 :global(.highlight) {
		color: white;
	}

	p.white {
		color: #e2f1fa;
	}

	.title-gap {
		height: 37px;
	}

	.small-gap {
		height: 12px;
	}
</style>
