<script>
	import ImageWithTextSection from './ImageWithTextSection.svelte';
	import PageLink from './PageLink.svelte';
	import { entries } from '$lib/servizi';
</script>

<ImageWithTextSection
	text="Con una visione ampia e d’insieme, il broker indipendente ha gli ha gli strumenti per creare la squadra giusta di esperti."
>
	{#snippet header()}
		Prediligiamo qualità e servizi su misura
	{/snippet}
	{#snippet illustration()}
		<div class="illustration">
			{#each entries as entry, i}
				<div class="rot-animation">
					<div class="pivot" style:rotate={`${(360 / entries.length) * i}deg`}>
						<div class="entry">{entry.title}</div>
					</div>
				</div>
			{/each}
		</div>
	{/snippet}
	{#snippet link()}
		<PageLink href={'/servizi'} label={'Servizi'}></PageLink>
	{/snippet}
</ImageWithTextSection>

<style>
	.illustration {
		width: 100%;
		height: 100%;
		background-color: #d3a26b36;
		overflow: hidden;
		position: relative;
	}

	@keyframes clockwiseRot {
		from {
			rotate: 0deg;
		}

		to {
			rotate: 360deg;
		}
	}

	.rot-animation {
		position: absolute;
		top: 50%;
		left: 50%;
		width: 0;
		height: 0;
		animation-duration: 120s;
		animation-name: clockwiseRot;
		animation-iteration-count: infinite;
		animation-direction: normal;
		animation-timing-function: linear;
	}

	.pivot {
		position: absolute;
		top: 0;
		left: 0;
		width: 0;
		height: 0;
	}

	.entry {
		font-weight: 700;
		white-space: nowrap;
		font-size: 30px;
		user-select: none;
		transform-origin: center left;
		position: absolute;
		top: -20px;
		left: 60px;
		color: white;
	}
</style>
