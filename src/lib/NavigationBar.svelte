<script lang="ts">
	import { page } from '$app/stores';
	import ChevronLeft from './icons/ChevronLeft.svelte';
	import ChevronRight from './icons/ChevronRight.svelte';
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

	let width = $state(0);
	let scrollWidth = $state(0);
	let scrollLeft = $state(0);
	function scrollWithArrows(el: HTMLElement) {
		$effect(() => {
			const resizeObserver = new ResizeObserver((entries) => {
				const entry = entries.at(0);
				if (entry) {
					width = entry.target.clientWidth;
					scrollWidth = entry.target.scrollWidth;
				}
			});
			resizeObserver.observe(el);

			el.onscroll = () => {
				scrollLeft = el.scrollLeft;
			};

			return () => resizeObserver.disconnect();
		});
	}
	const epsilon = 3;
	let isScrollable = $derived(scrollWidth > width);
	let leftIsOverflowing = $derived(scrollLeft > 0 + epsilon);
	let rightIsOverflowing = $derived(scrollLeft + width < scrollWidth - epsilon);
	let leftArrowIsVisible = $derived(isScrollable && leftIsOverflowing);
	let rightArrowIsVisible = $derived(isScrollable && rightIsOverflowing);

	let scrollEl: HTMLElement;
	let scrollByButtonAmount = $derived(width * 0.6);
	function scrollALittle(direction: 'left' | 'right') {
		const scrollAmount = scrollByButtonAmount * (direction === 'left' ? -1 : 1);
		scrollEl.scrollBy({ left: scrollAmount, behavior: 'smooth' });
	}
</script>

{#snippet scrollArrow(direction: 'left' | 'right')}
	<button
		class="scroll-arrow"
		class:left={direction === 'left'}
		class:right={direction === 'right'}
		class:visible={direction === 'left' ? leftArrowIsVisible : rightArrowIsVisible}
		onclick={() => scrollALittle(direction)}
	>
		<div class="arrow-icon-container">
			{#if direction === 'left'}
				<ChevronLeft />
			{:else}
				<ChevronRight />
			{/if}
		</div>
	</button>
{/snippet}

<nav>
	<div class="row-1">
		<a class="home-link" href="/">
			<div class="logo-container">
				<ViaVirtuosaLogo fillColor="accent" />
			</div>
			<div class="logo-text font-color-accent">Via Virtuosa</div>
		</a>
	</div>
	<div class="row-2" bind:this={scrollEl} use:scrollWithArrows>
		{@render scrollArrow('left')}
		{@render scrollArrow('right')}
		{#each navEntries as navEntry}
			{@const isCurrentPage = $page.route.id === navEntry.href}
			{@const flatSide = navEntry.flatRightSide && isCurrentPage}
			<NavigationBarLink href={navEntry.href} label={navEntry.label} {isCurrentPage} {flatSide} />
		{/each}
		<NavigationBarButton
			highlight={$page.route.id === navEntries[2].href}
			label="Prenota una Chiamata"
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

	.scroll-arrow {
		position: absolute;
		height: var(--nav-bar-button-height);
		width: 50px;
		display: grid;
	}

	.scroll-arrow:not(.visible) {
		display: none;
	}

	.scroll-arrow.left {
		left: 0;
		background: linear-gradient(90deg, var(--color-background) 70%, transparent 100%);
	}

	.scroll-arrow.right {
		right: 0;
		background: linear-gradient(270deg, var(--color-background) 70%, transparent 100%);
	}

	.arrow-icon-container {
		width: 24px;
		align-self: center;
		justify-self: center;
	}

	.arrow-icon-container :global(*) {
		stroke: #766347;
	}
</style>
