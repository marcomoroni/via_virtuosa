<script lang="ts">
	const navEntries = [
		{
			label: 'Servizi',
			href: '/servizi'
		},
		{
			label: 'La Storia',
			href: '/storia'
		},
		{
			label: 'Contatti',
			href: '/contatti'
		}
	];
</script>

<nav>
	{#each navEntries as navEntry}
		<a href={navEntry.href}>{navEntry.label}</a>
	{/each}
</nav>
