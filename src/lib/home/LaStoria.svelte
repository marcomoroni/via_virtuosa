<script>
	import PageLink from './PageLink.svelte';
</script>

<div class="grid">
	<img class="image" src="/images/Primo-Piano.jpg" alt="Luca Moroni a un convegno" />
	<div class="type">
		<h2 class="font-color-dark">Esperienza costruita negli anni</h2>
		<div class="title-gap"></div>
		<p class="font-color-light font-line-height-default">
			Via Virtuosa nasce nel 2008 dall’esperienza decennale del suo fondatore nel settore IT e Cyber
			Security.
		</p>
		<div class="small-gap"></div>
		<PageLink href={'/storia'} label={'La Storia'}></PageLink>
	</div>
</div>

<style>
	.grid {
		display: grid;
		grid-template-columns: var(--main-grid-template-columns);
		column-gap: var(--main-grid-column-gap);
	}

	.image {
		grid-column: 1 / 6;
		aspect-ratio: 1 / 1;
		object-fit: cover;
	}

	.type {
		grid-column: 6 / 9;
		padding-left: 40px;
		padding-right: 40px;
		align-self: center;
		text-wrap: balance;
	}

	h2 {
		font-size: 40px;
		line-height: 1.4;
		text-wrap: balance;
	}

	.title-gap {
		height: 37px;
	}

	.small-gap {
		height: 12px;
	}
</style>
