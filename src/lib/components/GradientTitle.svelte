<script>
	export let text = 'The possibilities are beyond your imagination';
	export let minSize = '2rem';
	export let vwSize = '6vw';
	export let maxSize = '3.4rem';
	export let gradient = 'linear-gradient(to right, #ae67fa, #f49867)';
	export let weight = 700;
	export let className = '';
</script>

<h2
	class="gradient-title {className}"
	style="
		--minSize: {minSize};
		--vwSize: {vwSize};
		--maxSize: {maxSize};
		--weight: {weight};
		--gradient: {gradient};
	"
>
	{text}
</h2>

<style>
	.gradient-title {
		width: 100%;
		font-size: clamp(var(--minSize), var(--vwSize), var(--maxSize));
		font-weight: var(--weight);
		background: var(--gradient);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		color: transparent;
		line-height: 1.2;
		word-break: break-word;
		margin: 0;
		display: inline-block;
	}

	/* Optional breathing animation */
	.breathing {
		animation: breathe 2.5s ease-in-out infinite;
		transform-origin: center;
	}

	@keyframes breathe {
		0%,
		100% {
			transform: scale(1);
			opacity: 0.85;
		}
		50% {
			transform: scale(1.1);
			opacity: 1;
		}
	}
</style>
