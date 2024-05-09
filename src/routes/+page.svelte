<script lang="ts">
	import LandingImage from '$lib/LandingImage.svelte';
</script>

<div class="nav-bar-gap"></div>

<div class="landing">
	<div class="image-container">
		<LandingImage />
	</div>
	<p class="landing-type font-color-accent">Il tuo cyber security personal trainer</p>
</div>

<p>
	<span class="font-color-accent">Via Virtuosa</span> è un aggregatore e acceleratore di competenze indipendente,
	focalizzato sui servizi di terza parte nei settori della Cyber Security e dell’IT Governance.
</p>

<style>
	.nav-bar-gap {
		height: 130px;
	}

	.landing {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		padding-left: var(--margin);
		padding-right: var(--margin);
	}

	.image-container {
		grid-column: 2 / 5;
		grid-row: 1 / 2;
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
</style>
