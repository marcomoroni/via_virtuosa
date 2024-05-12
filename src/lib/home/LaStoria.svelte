<script>
	import ImageWithTextSection from './ImageWithTextSection.svelte';
	import PageLink from './PageLink.svelte';
</script>

<ImageWithTextSection
	text="Via Virtuosa nasce nel 2008 dall’esperienza decennale del suo fondatore nel settore IT e Cyber
Security."
>
	{#snippet header()}
		Esperienza costruita negli anni
	{/snippet}
	{#snippet illustration()}
		<img class="image" src="/images/Infosek23_3_2.jpg" alt="Luca Moroni ad un convegno" />
	{/snippet}
	{#snippet link()}
		<PageLink href={'/storia'} label={'La Storia'}></PageLink>
	{/snippet}
</ImageWithTextSection>

<style>
	.image {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
