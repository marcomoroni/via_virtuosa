<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
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
</HorizontalMarginScaffold>

<style>
	.nav-bar-gap {
		height: 130px;
	}

	.section-gap {
		height: 150px;
	}
</style>
