<script lang="ts">
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import { headTitle } from '$lib/headTitle';

	const entries = [
		{
			title: 'Cyber security',
			intro: [
				'La sicurezza e la governance informatica sono aree di business che necessitano una ricerca continua in perimetri sempre più ampi. Il tema centrale è l’utilizzo di metodologie standard riconosciute (ISO, COBIT, ITIL, SOX, ECC). Per fornire un servizio ai massimi livelli servono competenza, rispetto alla sicurezza informatica, e un’IT governance che raramente convergono in un unico fornitore. Uno dei requisiti fondamentali per la sicurezza è garantire la rotazione dei valutatori che eseguono l’analisi. L’approccio più efficace è di tipo non convenzionale, con prodotti e servizi erogati entro l’Unione Europea.'
			],
			cosaFacciamo: [
				'Analisi di Sicurezza informatica e Penetration Test',
				'Sicurezza SCADA in produzione',
				'Copie forensi dei dati presenti sui dispositivi',
				'Stress Test per App con Back End',
				'Resilienza al Social Engineering (OSINT)',
				'Coaching indipendente sulla Cybersecurity',
				'Branch & Shop Breach',
				'Audit and Securizing Robot & IoT platform'
			]
		},
		{
			title: 'Audit IT e conformità',
			intro: [
				'La valutazione di una terza parte indipendente, attraverso gli audit, che non abbia un interesse focalizzato alla vendita di prodotti e soluzioni, è uno dei principi cardine del nostro servizio. L’obiettivo del revisore non è quello di sostituire i fornitori del cliente, ma eventualmente di rilevare le sue vulnerabilità. ',
				'Lo svolgimento di un audit, prima di un incidente o di una sanzione, riduce il rischio e l’entità del danno.',
				'La maturità sulla sicurezza, nella catena dei fornitori, è un obiettivo strategico.'
			],
			cosaFacciamo: [
				'Cyber Security Check (CIS 20)',
				'Audit normativo ISO/IEC 27001 22301 e Cobit e ITIL',
				'Web Application Penetration & Stress Test',
				'Perizie legali in caso di reati informatici',
				'Audit sulla compliance del processo di archiviazione sostitutiva',
				'Audit su installazioni database su base SQL e ORACLE',
				'Perizie Tecnologiche GDPR (a supporto Legal)',
				'Audit terzo ex ante su GDPR',
				'GDPR full Outsourcing'
			]
		},
		{
			title: 'Valutazione e scouting sicuro dei fornitori IT',
			intro: [
				'I fornitori e i vendor in ambito sicurezza informatica sono critici per l’azienda. I recenti incidenti insegnano che per arrivare all’obiettivo vero attacco la sua Supply Chain. Valutiamo la maturità dei fornitori critici attuali e i rischi nella migrazione o nella scelta di un nuovo ingresso nella catena di fornitura. La nostra proposta permette di valutare sia gli aspetti formali che la Qualità del Servizio erogato. Svolgiamo una valutazione come terza parte indipendente che non intende sostituirsi al fornitore valutato. L’obiettivo è creare dei KPI per identificare le criticità di chi gestisce i miei presidi di sicurezza e mi protegge.',
				'Garantiamo l’anonimato del cliente durante tutta la fase di scouting dei prodotti o servizi per la sicurezza attraverso una fitta rete di relazioni fra le aziende clienti.'
			],
			cosaFacciamo: [
				'Implicazioni di sicurezza nella migrazione in cloud',
				'Quality of Service Check del SOC in outsourcing',
				'Audit dell’Outsuorcer con metriche standard',
				'Sicurizzazione piattaforme Cloud (es. Exchange online)',
				'Audit Contrattualistica Cloud',
				'Supporto alla definizione e creazione delle Check List e delle Procedure di Procurement Sicuro',
				'Scouting riservato di soluzioni di Sicurezza (es. SIEM)',
				'Affiancamento Star o ISO 27017/18'
			]
		},
		{
			title: 'Azienda sicura',
			intro: [
				'Valutare un grado adeguato di business continuity è un’operazione da prendere seriamente. Nella catena della sicurezza bisogna essere attenti dal piccolo dispositivo mobile al grande sito di produzione. Spesso l’anello più debole della catena viene sottovalutato. In un incidente informatico il danno più grave è il danno indiretto che incide sulla reputazione. Il fattore umano è una criticità che viene mitigata da un’adeguata formazione e consapevolezza. Una copertura del rischio residuo tutela l’azienda con una corretta assicurazione cyber. La giusta valutazione complessiva del processo cyber può essere fatta solo da chi è estraneo alla vendita di prodotti e/o servizi collegati alla problematica.'
			],
			cosaFacciamo: [
				'Audit del processo di DR e BC',
				'Disaster Recovery Plan secondo la norma 22301',
				'Segregation of Duties (eg. SAP Security)',
				'Business Impact Analysis',
				'Cancellazione sicura',
				'Creazione Forensic Interna',
				'Valutazione rischio residuo e polizze Cyber Risk',
				'Gestione della crisi per incidente Cyber',
				'Shadow IT mitigation (es. Audit neutri di progetti ERP ex ante ed ex post)'
			]
		},
		{
			title: 'Flusso digitale sicuro',
			intro: [
				'I dati e le informazioni aziendali sono il tesoro più prezioso dell’azienda: vanno protetti e difesi. L’obiettivo di questa area di business è identificare il canale digitale più sicuro per il flusso di informazioni. Non è sempre necessario sostituire la piattaforma esistente, ma adattare l’esistente con un approccio oggettivo. I framework, come la certificazione ISO 27001 o il NIST, sono validi supporti per una comunicazione più sicura. La mitigazione e protezione dalle frodi digitali sarà la sfida dei prossimi anni.'
			],
			cosaFacciamo: [
				'Digital Brand Reputation Abuse Discovery',
				'Protezione del patrimonio informativo aziendale',
				'Criptazione delle comunicazioni',
				'Simulazione spionaggio industriale',
				'Supporto alla definizione e creazione delle Check List e delle Procedure di Cybersecurity',
				'GA 27001 sui processi di gestione documentale',
				'Corsi avanzati di codice sicuro',
				'Code Review di App e Applicazioni Web',
				'Cybersecurity per AEO DOGANE'
			]
		},
		{
			title: 'Governance IT',
			intro: [
				'L’utilizzo della tecnologia nei processi aziendali è sempre più pervasivo. Il rischio più grande è perdere il controllo. Per evitare il caos è necessario avere una visione chiara e completa delle risorse. L’obiettivo principale è misurare l’efficienza, individuando i problemi critici nei processi IT. Il nostro sogno è creare una dashboard aggiornata in tempo reale sui possibili rischi. La crescita e il miglioramento del controllo devono essere in costante evoluzione.'
			],
			cosaFacciamo: [
				'Valutazione dei fornitori sulla postura di sicurezza',
				'Audit di Sicurezza dei dispositivi mobili',
				'Assets Inventory & Monitoring',
				'Definizione Security Policy in ambito Mobile',
				'Gestione dell’incidente Informatico',
				'Creazione Blue Team interno',
				'Drafting di Policy ISA 99 62443 di Cybersecurity in area produzione',
				'Data Loss Prevention e Data Right Management',
				'Soluzioni di GRC (es. per GDPR)'
			]
		}
	];
</script>

<svelte:head>
	<title>{headTitle('Servizi')}</title>
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
						{#each entry.intro as introParagraph}
							<p class="font-color-light font-line-height-default">{introParagraph}</p>
						{/each}
						<h3 class="font-color-dark font-line-height-default">Cosa facciamo?</h3>
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

	h3 {
		margin-top: 33px;
		margin-bottom: 15px;
		font-size: 20px;
		text-wrap: balance;
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
