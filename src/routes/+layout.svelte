<script lang="ts">
	import '../styles/reset.css';

	let { children } = $props();
</script>

<svelte:head>
	<title>Via Virtuosa</title>
</svelte:head>

{@render children()}
