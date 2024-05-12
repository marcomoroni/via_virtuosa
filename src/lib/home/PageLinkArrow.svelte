<script lang="ts">
	let { color = 'accent' }: { color?: 'accent' | 'blue' } = $props();
</script>

<svg
	width="22"
	height="12"
	viewBox="0 0 22 12"
	fill="none"
	xmlns="http://www.w3.org/2000/svg"
	class:blue={color === 'blue'}
>
	<path
		fill-rule="evenodd"
		clip-rule="evenodd"
		d="M16.7574 0.696721L21.5303 5.46969C21.8232 5.76258 21.8232 6.23746 21.5303 6.53035L16.7574 11.3033C16.4645 11.5962 15.9896 11.5962 15.6967 11.3033C15.4038 11.0104 15.4038 10.5356 15.6967 10.2427L19.1893 6.75002H0V5.25002H19.1893L15.6967 1.75738C15.4038 1.46449 15.4038 0.989614 15.6967 0.696721C15.9896 0.403827 16.4645 0.403827 16.7574 0.696721Z"
	/>
</svg>

<style>
	path {
		fill: var(--color-accent);
	}

	.blue path {
		fill: var(--color-csa-blue);
	}
</style>
