<script lang="ts">
	import HorizontalMarginScaffold from './HorizontalMarginScaffold.svelte';
</script>

<HorizontalMarginScaffold>
	<div class="container font-weight-default">
		<div class="line">Copyright © 2024 ViaVirtuosa Srl; all rights reserved</div>
		<div class="line">Via Benedetto Croce, 3, Schio (VI) 36015 Italy</div>
		<div class="line">P.IVA 03979730243</div>
		<div class="line">tao@viavirtuosa.it</div>
		<div class="line">Cookies free</div>
	</div>
</HorizontalMarginScaffold>

<style>
	.container {
		text-align: center;
		margin-bottom: 30px;
		color: #c2bcb3;
		display: flex;
		flex-direction: row;
		gap: 18px;
		justify-content: center;
	}

	.line {
		font-size: 12px;
	}

	@media (max-width: 1050px) {
		.container {
			flex-direction: column;
			gap: 4px;
		}
	}
</style>
