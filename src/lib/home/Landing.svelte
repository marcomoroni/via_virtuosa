<script lang="ts">
	import LandingImage from '$lib/home/LandingImage.svelte';

	let { landingType }: { landingType: string } = $props();
</script>

<div class="landing">
	<div class="image-container">
		<LandingImage />
	</div>
	<p class="landing-type font-color-accent">{landingType}</p>
</div>

<style>
	.landing {
		display: grid;
		grid-template-columns: var(--main-grid-template-columns);
		column-gap: var(--main-grid-column-gap);
	}

	.image-container {
		grid-column: 3 / 9;
		grid-row: 1 / 2;
		position: relative;
	}

	.landing-type {
		grid-column: 1 / 5;
		grid-row: 1 / 2;
		font-size: 60px;
		font-weight: 700;
		text-wrap: balance;
		z-index: 1;
		margin-top: 35px;
		margin-bottom: 35px;
	}

	@media (max-width: 1330px) {
		.landing {
			grid-template-columns: unset;
		}

		.image-container {
			grid-column: unset;
			grid-row: 2 / 3;
		}

		.landing-type {
			grid-column: unset;
			grid-row: 1 / 2;
			font-size: 42px;
			max-width: 680px;
			text-align: center;
			justify-self: center;
		}
	}
</style>
