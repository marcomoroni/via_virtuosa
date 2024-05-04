<script lang="ts">
	let {
		href,
		label,
		isCurrentPage,
		flatSide
	}: { href: string; label: string; isCurrentPage: boolean; flatSide: boolean } = $props();
</script>

<a
	{href}
	class="font-size-default font-weight-default font-color-dark"
	class:is-current-page={isCurrentPage}
	class:flat-side={flatSide}
>
	{label}
</a>

<style>
	a {
		--horizontal-padding: 26px;
		--vertical-padding: 19px;
		padding-left: var(--horizontal-padding);
		padding-right: var(--horizontal-padding);
		padding-top: var(--vertical-padding);
		padding-bottom: var(--vertical-padding);
		text-wrap: nowrap;
		display: grid;
		border-radius: calc(infinity * 1px);
	}

	.is-current-page {
		background-color: white;
	}

	.flat-side {
		border-top-right-radius: 0;
		border-bottom-right-radius: 0;
	}
</style>
