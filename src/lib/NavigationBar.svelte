<script lang="ts">
	import { page } from '$app/stores';
	import NavigationBarButton from './NavigationBarButton.svelte';
	import NavigationBarLink from './NavigationBarLink.svelte';
	import ViaVirtuosaLogo from './ViaVirtuosaLogo.svelte';

	const navEntries = [
		{
			label: 'Servizi',
			href: '/servizi',
			flatRightSide: false
		},
		{
			label: 'La Storia',
			href: '/storia',
			flatRightSide: false
		},
		{
			label: 'Contatti',
			href: '/contatti',
			flatRightSide: true
		}
	];
</script>

<nav>
	<div class="row-1">
		<a class="home-link" href="/">
			<div class="logo-container">
				<ViaVirtuosaLogo fillColor="accent" />
			</div>
			<div class="logo-text font-color-accent">Via Virtuosa</div>
		</a>
	</div>
	<div class="row-2">
		{#each navEntries as navEntry}
			{@const isCurrentPage = $page.route.id === navEntry.href}
			{@const flatSide = navEntry.flatRightSide && isCurrentPage}
			<NavigationBarLink href={navEntry.href} label={navEntry.label} {isCurrentPage} {flatSide} />
		{/each}
		<NavigationBarButton
			label="Prenota una chiamata"
			highlight={$page.route.id === navEntries[2].href}
			href="https://koalendar.com/e/incontro-con-luca-moroni"
		/>
	</div>
</nav>

<style>
	nav {
		min-height: 0;
		width: 100%;
		display: flex;
		flex-direction: column;
		overflow-x: hidden;
	}

	nav :global(*) {
		--border-radius-transition: border-radius 0.9s ease-out;
	}

	.row-1 {
		align-self: center;
	}

	.row-2 {
		align-self: center;
		min-width: 0;
		display: flex;
		flex-direction: row;
		gap: 9px;
		overflow-x: scroll;
		scrollbar-width: none;
		max-width: 100%;
		padding-left: 30px;
		padding-right: 30px;
	}

	.home-link {
		min-height: 0;
		display: flex;
		flex-direction: column;
		gap: 23px;
		padding: 20px;
		margin-top: 33px;
		margin-bottom: 24px;
	}

	.logo-container {
		width: 112px;
		align-self: center;
	}

	.logo-text {
		font-size: 32px;
		font-weight: 600;
		text-align: center;
		align-self: center;
		text-wrap: nowrap;
		user-select: none;
	}
</style>
