<script lang="ts">
	let {
		href,
		label,
		isCurrentPage,
		flatSide
	}: { href: string; label: string; isCurrentPage: boolean; flatSide: boolean } = $props();
</script>

<a {href} class:is-current-page={isCurrentPage} class:flat-side={flatSide}>
	<div class="label font-size-default font-weight-default font-color-dark">
		{label}
	</div>
</a>

<style>
	a {
		--horizontal-padding: 22px;
		padding-left: var(--horizontal-padding);
		padding-right: var(--horizontal-padding);
		height: 52px;
		display: grid;
		border-radius: calc(infinity * 1px);
		transition: var(--border-radius-transition);
		display: grid;
	}

	.label {
		text-wrap: nowrap;
		align-self: center;
		justify-self: center;
	}

	.is-current-page {
		background-color: white;
	}

	.flat-side {
		border-top-right-radius: 0;
		border-bottom-right-radius: 0;
	}
</style>
