<script>
	import HorizontalMarginScaffold from '$lib/HorizontalMarginScaffold.svelte';
	import ViaVirtuosaLogo from '$lib/ViaVirtuosaLogo.svelte';
	import { headTitle } from '$lib/headTitle';
</script>

<svelte:head>
	<title>{headTitle('La Storia')}</title>
	<meta name="description" content="Come è nata Via Virtuosa" />
</svelte:head>

<div class="nav-bar-gap"></div>

<HorizontalMarginScaffold>
	<div class="illustation-container">
		<div class="illustation-2">
			<ViaVirtuosaLogo fillColor="dim" />
		</div>
		<div class="illustation-1">
			<img
				src="/images/immagine-strada.png"
				alt="ClipArt che ha ispirato il logo di Via Virtuosa"
			/>
		</div>
	</div>
	<div class="type-container">
		<p class="font-color-light font-line-height-default font-weight-default">
			Nel 2008 avevo raggiunto una mansione di responsabilità ed ero un quadro all’interno di una
			azienda. Per una serie di motivi, il progetto è decaduto e mi sono trovato davanti ad una
			scelta difficile.
			<strong>
				Continuare a lavorare come dipendente a metà dello stipendio o uscire e ricominciare da zero
				a 43 anni.
			</strong>
			Ho scelto di ricominciare con una componente di rischio molto alta. Cercare di reinventarsi non
			è facile ma le esperienze di imprenditore dopo la laurea mi hanno aiutato.
		</p>
		<p class="font-color-light font-line-height-default font-weight-default">
			Durante quei giorni pensavo che avrei dovuto evitare di percorrere una strada che mi avrebbe
			potuto far tornare al punto di partenza (il Via del Monopoli per chi lo conosce).
		</p>
		<p class="font-color-light font-line-height-default font-weight-default">
			Cercando una idea diversa mi sono imbattuto in una vecchia illustrazione di Windows con un
			uomo davanti ad un bivio. Non so chi di voi se la ricorda o l’ha mai vista? Sicuramente solo
			gli x-enta o gli x-anta. Direi che lei ha trovato me. Ho pensato di iniziare una nuova via e
			mi sono figurato di essere il numero civico 1. Quello è il primo insediamento che trovi
			iniziando una nuova strada. Nel 2008 il termine Virtuoso non era molto usato,
			<strong>ma oggi sento che sta arrivando un nuovo rinascimento</strong>
			. Percorrere strade tortuose senza una meta precisa non era più il tempo. Per cui è da questo incontro
			casuale con con questa illustrazione di Windows (davanti a tanti problemi) che sono partito. Via
			Virtuosa fonde in un logo le due lettere V schizzando quella vecchia illustrazione che non si trova
			più. Oggi devo dire che l’istinto mi ha dato ragione. Ma se la Via è dritta è comunque in salita,
			per cui sempre dura. Ogni tanto mi giro a vedere la strada percorsa e da dove sono partito. Dedico
			questo pensiero anche alle persone che incuriosite dal nome mi chiedono il significato in un mondo
			di Tech..., Sys…, Serv…,  Sec…, Via Virtuosa è disruptive. Ancora oggi al telefono le persone mi
			chiedono di ripetere il nome perché sono abituati a sentire Tech.., Sys…, Serv…, Sec… Auguro a
			tutti quelli che sono davanti ad una scelta di vita di trovare la loro Via Virtuosa.
		</p>
		<div class="signature font-line-height-default font-weight-default">
			Luca Moroni — CEO Via Virtuosa
		</div>
	</div>
</HorizontalMarginScaffold>

<div class="bottom-gap"></div>

<style>
	.nav-bar-gap {
		height: 150px;
	}

	.bottom-gap {
		height: 200px;
	}

	.illustation-container {
		display: grid;
		grid-template-columns: 3fr 1fr 1.9fr;
		grid-template-rows: 2fr 1fr 2fr;
		margin-bottom: 90px;
		max-width: 1100px;
		margin-left: auto;
		margin-right: auto;
	}

	.illustation-1 {
		grid-row: 1 / 3;
		grid-column: 1 / 3;
	}

	.illustation-2 {
		grid-row: 2 / 4;
		grid-column: 2 / 4;
	}

	@media (max-width: 660px) {
		.illustation-container {
			grid-template-columns: unset;
			grid-template-rows: unset;
		}

		.illustation-1 {
			grid-row: unset;
			grid-column: unset;
		}

		.illustation-2 {
			display: none;
		}
	}

	.type-container {
		max-width: 700px;
		margin-left: auto;
		margin-right: auto;
	}

	.signature {
		color: #aa9f90;
		margin-top: 30px;
		text-align: right;
	}
</style>
