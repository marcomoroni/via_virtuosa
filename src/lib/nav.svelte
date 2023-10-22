<script lang="ts">
	import WidthContainer from './WidthContainer.svelte';

	export let absolutePos: boolean;
</script>

<nav class:absolute-pos={absolutePos}>
	<WidthContainer>
		<div class="links">
			<a href="/">Via Virtuosa</a>
			<a href="/servizi">Servizi</a>
			<!-- <a href="/storia">La storia</a> -->
			<!-- <a href="/pubblicazioni">Pubblicazioni</a> -->
			<a href="/contatti">Contatti</a>
		</div>
	</WidthContainer>
</nav>

<style>
	nav {
		width: 100%;
	}

	a {
		white-space: nowrap;
	}

	.absolute-pos {
		position: absolute;
	}

	.links {
		height: 60px;
		display: flex;
		flex-direction: row;
		width: 100%;
		align-items: center;
		justify-content: flex-start;
		gap: 20px;
	}

	@media (max-width: 550px) {
		nav {
			/* todo: mobile */
			display: none;
			background-color: red;
		}
	}
</style>
