<script>
	export let title = 'What is GPT?';
	export let width = 38; // line width in px
	export let height = 3; // line height in px
	export let colorStart = '#AE67FA';
	export let colorEnd = '#F49867';

	// NEW — allows you to change the text size
	export let fontSize = '2rem';
</script>

<div
	class="heading-with-line"
	style="
    --width: {width}px;
    --height: {height}px;
    --colorStart: {colorStart};
    --colorEnd: {colorEnd};
    --fontSize: {fontSize};
  "
>
	<h3>{title}</h3>
</div>

<style>
	h3 {
		font-size: var(--fontSize); /* now dynamic */
		font-weight: 700;
		color: #fff;
		line-height: 1;
		white-space: nowrap;
		margin: 0;
	}

	.heading-with-line {
		position: relative;
		display: inline-block;
	}

	.heading-with-line::after {
		content: '';
		position: absolute;
		bottom: 100%;
		left: 0;
		margin-bottom: 1em;

		width: var(--width);
		height: var(--height);
		border-radius: var(--height);
		background: linear-gradient(to bottom right, var(--colorStart), var(--colorEnd));

		animation: breathe 2.5s ease-in-out infinite;
		transform-origin: center;
	}

	@keyframes breathe {
		0%,
		100% {
			transform: scaleX(1) scaleY(1);
			opacity: 0.8;
		}
		50% {
			transform: scaleX(1.2) scaleY(1.2);
			opacity: 1;
		}
	}
</style>
