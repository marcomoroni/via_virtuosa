<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import { headTitle } from '$lib/headTitle';
	import { entries } from '$lib/servizi';
</script>

<svelte:head>
	<title>{headTitle('Servizi')}</title>
	<meta name="description" content="Come ti supportiamo" />
</svelte:head>

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<div class="list">
		{#each entries as entry}
			<div class="container-for-bar">
				<div class="bar"></div>
				<div class="inner">
					<div class="title-container">
						<h2 class="title font-color-accent">{entry.title}</h2>
						<div class="fade"></div>
					</div>
					<div class="content-container">
						<ul class="list-with-disc">
							{#each entry.cosaFacciamo as cosaFacciamoEntry}
								<li class="font-color-light">{cosaFacciamoEntry}</li>
							{/each}
						</ul>
					</div>
				</div>
			</div>
		{/each}
	</div>
</HorizontalMarginScaffold>

<style>
	.nav-bar-gap {
		height: 150px;
	}

	.list {
		min-height: 0;
		display: flex;
		flex-direction: column;
		gap: 140px;
		--bar-thickness: 5px;
		margin-bottom: 200px;
	}

	.container-for-bar {
		min-height: 0;
		display: flex;
		flex-direction: column;
	}

	.bar {
		flex-basis: var(--bar-thickness);
		background-color: var(--color-accent);
		align-self: stretch;
		position: sticky;
		top: 0;
	}

	.inner {
		display: grid;
		grid-template-columns: 400px 1fr;
	}

	.title-container {
		grid-column: 1 / 2;
		position: sticky;
		padding-top: 27px;
		top: var(--bar-thickness);
		align-self: start;
	}

	li {
		line-height: 1.9;
	}

	.content-container {
		grid-column: 2 / 3;
		padding-top: 42px;
		padding-left: 80px;
		padding-right: 80px;
	}

	.title {
		font-size: 32px;
		font-weight: 700;
		line-height: 1.4;
	}

	.fade {
		display: none;
	}

	@media (max-width: 1250px) {
		.inner {
			display: grid;
			grid-template-columns: unset;
		}

		.title-container {
			grid-column: unset;
			grid-row: 1/2;
			background-color: var(--color-background);
			padding-bottom: 15px;
		}

		.content-container {
			grid-column: unset;
			grid-row: 2/3;
			padding-left: unset;
			padding-right: unset;
		}

		.fade {
			display: unset;
			--height: 30px;
			background: linear-gradient(var(--color-background), transparent);
			position: absolute;
			bottom: calc(var(--height) * -1);
			left: 0;
			height: var(--height);
			width: 100%;
		}
	}

	@media (max-width: 700px) {
		.list {
			margin-bottom: 60px;
		}
	}
</style>
