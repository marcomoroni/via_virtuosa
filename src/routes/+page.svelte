<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import Landing from '$lib/home/Landing.svelte';
	import WhatIsViaVirtuosa from '$lib/home/WhatIsViaVirtuosa.svelte';
</script>

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<Landing />

	<div class="section-gap"></div>

	<WhatIsViaVirtuosa />

	<div class="section-gap"></div>
</HorizontalMarginScaffold>

<style>
	.nav-bar-gap {
		height: 130px;
	}

	.section-gap {
		height: 150px;
	}
</style>
