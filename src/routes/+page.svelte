<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import LaStoria from '$lib/home/LaStoria.svelte';
	import Landing from '$lib/home/Landing.svelte';
	import WhatIsViaVirtuosa from '$lib/home/WhatIsViaVirtuosa.svelte';
</script>

{#snippet sectionGap()}
	<div class="section-gap"></div>
{/snippet}

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<Landing />
	{@render sectionGap()}
	<WhatIsViaVirtuosa />
	{@render sectionGap()}
	<div class="line"></div>
	{@render sectionGap()}
	<LaStoria />
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
