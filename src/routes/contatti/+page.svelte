<script>
	import ContactsEntry from '$lib/ContactsEntry.svelte';
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import { headTitle } from '$lib/headTitle';
	import LinkedIn from '$lib/icons/LinkedIn.svelte';
	import Mail from '$lib/icons/Mail.svelte';
	import MapPin from '$lib/icons/MapPin.svelte';
	import Phone from '$lib/icons/Phone.svelte';
	import YouTube from '$lib/icons/YouTube.svelte';
</script>

<svelte:head>
	<title>{headTitle('Contatti')}</title>
	<meta name="description" content="Fai due chiacchere con Luca Moroni" />
</svelte:head>

<HorizontalMarginScaffold>
	<ul class="contacts-list">
		<ContactsEntry href="https://www.linkedin.com/company/via-virtuosa/">
			{#snippet icon()}
				<LinkedIn />
			{/snippet}
			{#snippet text()}
				LinkedIn
			{/snippet}
		</ContactsEntry>
		<ContactsEntry href="https://www.youtube.com/@viavirtuosa">
			{#snippet icon()}
				<YouTube />
			{/snippet}
			{#snippet text()}
				YouTube
			{/snippet}
		</ContactsEntry>
		<ContactsEntry href="mailto:tao@viavirtuosa.it">
			{#snippet icon()}
				<Mail />
			{/snippet}
			{#snippet text()}
				tao@viavirtuosa.it
			{/snippet}
		</ContactsEntry>
		<ContactsEntry href="tel:+393386258675">
			{#snippet icon()}
				<Phone />
			{/snippet}
			{#snippet text()}
				+39 3386258675
			{/snippet}
		</ContactsEntry>
		<ContactsEntry href={undefined}>
			{#snippet icon()}
				<MapPin />
			{/snippet}
			{#snippet text()}
				Via Benedetto Croce, 3, Schio (VI) 36015 Italy
			{/snippet}
		</ContactsEntry>
	</ul>
</HorizontalMarginScaffold>

<style>
	.contacts-list {
		margin-top: 150px;
		margin-bottom: 200px;
		display: grid;
		grid-auto-flow: row;
		grid-auto-rows: 1fr;
		row-gap: 15px;
		max-width: 700px;
		margin-left: auto;
		margin-right: auto;
	}
</style>
