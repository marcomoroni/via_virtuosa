<script lang="ts">
	import WidthContainer from '$lib/WidthContainer.svelte';
</script>

<div class="landing">
	<div class="landing-padding-top" />
	<WidthContainer>
		<div class="logo" />
		<h1 class="name">Via Virtuosa</h1>
		<p class="a">Il tuo cyber security personal trainer</p>
		<p class="b">
			Via Virtuosa è un aggregatore e acceleratore di competenze indipendente, focalizzato sui
			servizi di terza parte nei settori della Cyber Security e dell’IT Governance.
		</p>
	</WidthContainer>
	<div class="landing-padding-bottom" />
</div>

<style>
	.landing {
		min-height: 100dvh;
		display: flex;
		flex-direction: column;
	}

	.landing-padding-top,
	.landing-padding-bottom {
		flex: 1;
	}

	.landing-padding-top {
		flex: 1;
		min-height: 90px;
	}

	.landing-padding-bottom {
		min-height: 60px;
	}

	.logo {
		width: 450px;
		aspect-ratio: 3 / 2;
		border: 1px solid black;
	}

	.name,
	.a,
	.b {
		max-width: 80%;
		text-wrap: balance;
	}

	.name {
		font-size: 60px;
		font-weight: 450;
		margin-top: 20px;
		white-space: nowrap;
	}

	.a {
		font-size: 26px;
		font-weight: 450;
		margin-top: 20px;
	}

	.b {
		font-size: 20px;
		margin-top: 50px;
		color: #7d5f31;

		/* Move all the landing content a little up. */
		padding-bottom: 10px;
	}

	@media (max-width: 550px) {
		.logo {
			width: 400px;
		}
	}

	@media (max-width: 450px) {
		.logo {
			width: 300px;
		}
	}

	@media (max-width: 350px) {
		.logo {
			width: 220px;
		}
	}

	@media (max-width: 260px) {
		.logo {
			width: 150px;
		}
	}

	@media (max-width: 660px) {
		.name,
		.a,
		.b {
			max-width: unset;
		}

		.name {
			font-size: 40px;
			margin-top: 17px;
		}

		.a {
			font-size: 22px;
			margin-top: 8px;
		}

		.b {
			font-size: 16px;
			margin-top: 30px;
		}
	}
</style>
