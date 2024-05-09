<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import LandingImage from '$lib/LandingImage.svelte';
</script>

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<div class="landing">
		<div class="image-container">
			<LandingImage />
		</div>
		<p class="landing-type font-color-accent">Il tuo cyber security personal trainer</p>
	</div>

	<div class="section-gap"></div>

	<p>
		<span class="font-color-accent">Via Virtuosa</span> è un aggregatore e acceleratore di competenze
		indipendente, focalizzato sui servizi di terza parte nei settori della Cyber Security e dell’IT Governance.
	</p>
</HorizontalMarginScaffold>

<style>
	.nav-bar-gap {
		height: 130px;
	}

	.section-gap {
		height: 150px;
	}

	.landing {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
	}

	.image-container {
		grid-column: 2 / 5;
		grid-row: 1 / 2;
		position: relative;
	}

	.landing-type {
		grid-column: 1 / 3;
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
