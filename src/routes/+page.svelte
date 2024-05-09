<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import Landing from '$lib/Landing.svelte';
</script>

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<Landing />

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
</style>
