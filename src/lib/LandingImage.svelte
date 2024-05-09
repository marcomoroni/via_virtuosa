<div class="stack">
	<div class="layer-image">
		<img
			class="hochosterwitz"
			src="/images/hochosterwitz-4423670_1920.jpg"
			alt="Castello di Hochosterwitz"
		/>
	</div>
	<div class="layer-tint"></div>
	<div class="layer-fade"></div>
</div>

<style>
	.stack {
		position: relative;
		width: 100%;
		aspect-ratio: 912 / 728;
		min-height: 600px;
	}

	.layer-image,
	.layer-tint,
	.layer-fade {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}

	.layer-tint {
		background-color: var(--color-accent);
		mix-blend-mode: hue;
	}

	.layer-fade {
		height: 18%;
		background: linear-gradient(var(--color-background), transparent);
	}

	.hochosterwitz {
		width: 100%;
		height: 100%;
		object-fit: cover;
		filter: brightness(125%) contrast(115%);
		opacity: 0.9;
	}
</style>
