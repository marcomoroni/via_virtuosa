<script lang="ts">
	import WidthContainer from '$lib/WidthContainer.svelte';

	const tiSupportiamoCon = [
		{
			title: 'Cyber security',
			text: 'La sicurezza e la governance informatica sono aree di business che necessitano una ricerca continua in perimetri sempre più ampi utilizzando metologie riconosciute.'
		},
		{
			title: 'Audit IT e conformità',
			text: 'La valutazione di una terza parte indipendente, che non abbia un interesse focalizzato alla vendita è uno dei principi cardine del nostro servizio.'
		},
		{
			title: 'Valutazione e scouting sicuro dei fornitori IT',
			text: 'I fornitori IT che si occupano di sicurezza informatica sono degli elementi critici ed è importante non sbagliare e verificarne sempre l’efficienza e l’efficacia.'
		},
		{
			title: 'Azienda sicura',
			text: 'Nella catena della sicurezza bisogna essere attenti dal piccolo dispositivo mobile al grande sito di produzione. Spesso l’anello più debole della catena viene sottovalutato.'
		},
		{
			title: 'Flusso digitale sicuro',
			text: 'I dati e le informazioni aziendali sono il tesoro più prezioso dell’azienda: vanno protetti e difesi. La mitigazione e protezione dalle frodi digitali sarà la sfida dei prossimi anni.'
		},
		{
			title: 'Governance IT',
			text: 'L’utilizzo della tecnologia nei processi aziendali è sempre più pervasivo. L’obiettivo principale è misurare l’efficienza, individuando i problemi critici nei processi IT.'
		}
	];
</script>

<WidthContainer>
	<h1>Servizi</h1>

	<p>
		I miei competitor fanno analisi di sicurezza e valutazioni e poi vendono prodotti di Cyber
		Security o servizi gestiti (sono <span class="special">farmacisti</span>) io faccio solo
		valutazioni e non vendo prodotti o servizi per fare la remediation (sono un
		<span class="special">Dottore</span>).
	</p>
	<p>
		La domanda è, se vai a fare una visita (analisi sullo stato di sicurezza della tua azienda) per
		sapere che malattie hai, ti rivolgi al farmacista o al dottore?
	</p>
	<h2>Ti supportiamo con</h2>
	<ul class="ti-supportiamo-con-grid">
		{#each tiSupportiamoCon as { title, text }}
			<li class="ti-supportiamo-con-entry">
				<h3 class="ti-supportiamo-con-title">{title}</h3>
				<p class="ti-supportiamo-con-text">{text}</p>
			</li>
		{/each}
	</ul>
</WidthContainer>

<style>
	.special {
		font-weight: 700;
	}

	.ti-supportiamo-con-grid {
		display: grid;
		grid-auto-flow: row;
		grid-template-columns: 1fr 1fr 1fr;
		grid-auto-rows: 1fr;
		gap: var(--horizontal-margin);
		margin-top: 40px;
		margin-bottom: 80px;
	}

	@media (max-width: 850px) {
		.ti-supportiamo-con-grid {
			grid-template-columns: 1fr 1fr;
		}
	}

	@media (max-width: 550px) {
		.ti-supportiamo-con-grid {
			grid-template-columns: 1fr;
		}
	}

	.ti-supportiamo-con-entry {
		background-color: #e5bc7e;
		padding: 20px;
	}

	.ti-supportiamo-con-title {
		font-size: 18px;
		font-weight: 600;
		margin-bottom: 15px;
	}

	.ti-supportiamo-con-text {
		color: #7d5f31;
	}
</style>
