<script lang="ts">
	import '../styles/reset.css';
	import NavigationBar from '$lib/NavigationBar.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<title>Via Virtuosa</title>
</svelte:head>

<NavigationBar />

{@render children()}
