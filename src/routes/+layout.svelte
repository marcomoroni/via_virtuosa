<script lang="ts">
	import '../styles/reset.css';
	import '../styles/main.css';
	import NavigationBar from '$lib/NavigationBar.svelte';
	import Footer from '$lib/Footer.svelte';

	let { children } = $props();
</script>

<NavigationBar />

{@render children()}

<Footer />
