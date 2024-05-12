<script lang="ts">
	import ImageWithTextSection from './ImageWithTextSection.svelte';
	import PageLink from './PageLink.svelte';
</script>

<ImageWithTextSection
	background="blue"
	illustrationBackgroundColor="white"
	text="Abbiamo creato Cyber Security Angels, una rete di sole aziende finali in cui non sono ammessi Vendor e Integratori sui temi della Cybersecurity e IT Governance al fine di far fronte comune agli incidenti di cyber security e fare networking sul territorio."
>
	{#snippet header()}
		Difendi Il tuo castello insieme ai <span class="highlight">Cyber Security Angels</span>
	{/snippet}
	{#snippet illustration()}
		<div class="logo-container">
			<img class="logo" src="/images/CSA.png" alt="Logo di Cyber Security Angels" />
		</div>
	{/snippet}
	{#snippet link()}
		<PageLink
			href={'https://www.cybersecurityangels.it/'}
			label={'Entra nella cyber community'}
			color="blue"
		></PageLink>
	{/snippet}
</ImageWithTextSection>

<style>
	.logo-container {
		width: 100%;
		height: 100%;
		background-color: white;
		display: grid;
		padding: 40px;
	}

	.logo {
		justify-self: center;
		align-self: center;
		width: 100%;
		max-width: 380px;
	}
</style>
