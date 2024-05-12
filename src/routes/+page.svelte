<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import CyberSecurityAngles from '$lib/home/CyberSecurityAngles.svelte';
	import LaStoria from '$lib/home/LaStoria.svelte';
	import Landing from '$lib/home/Landing.svelte';
	import Servizi from '$lib/home/Servizi.svelte';
	import WhatIsViaVirtuosa from '$lib/home/WhatIsViaVirtuosa.svelte';

	const landingType = 'Il tuo cyber security personal trainer';
</script>

<svelte:head>
	<title>Via Virtuosa</title>
	<meta name="description" content={landingType} />
</svelte:head>

{#snippet sectionGap()}
	<div class="section-gap"></div>
{/snippet}

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<Landing {landingType} />
	{@render sectionGap()}
	<WhatIsViaVirtuosa />
	{@render sectionGap()}
	<div class="line"></div>
	{@render sectionGap()}
	<LaStoria />
	{@render sectionGap()}
	<Servizi />
	{@render sectionGap()}
	<CyberSecurityAngles />
	{@render sectionGap()}
</HorizontalMarginScaffold>

<style>
	.nav-bar-gap {
		height: 130px;
	}

	.section-gap {
		height: 150px;
	}

	.line {
		height: 5px;
		width: 100%;
		background-color: #dfd5c9;
	}
</style>
