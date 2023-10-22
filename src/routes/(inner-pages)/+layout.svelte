<script lang="ts">
	import Nav from '$lib/Nav.svelte';
</script>

<Nav absolutePos={false} />

<slot />

<style>
	:global(h1) {
		margin-top: 140px;
		margin-bottom: 70px;
		font-size: 40px;
		font-weight: 500;
	}

	:global(h2) {
		margin-top: 50px;
		margin-bottom: 30px;
		font-size: 28px;
		font-weight: 500;
	}

	:global(p) {
		margin-top: 9px;
		margin-bottom: 9px;
	}
</style>
