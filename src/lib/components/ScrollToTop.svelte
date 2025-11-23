<script>
	import ArrowUpIcon from '$lib/assets/arrow-up.svg';
	import { onMount } from 'svelte';
	// Your arrow SVG

	let isVisible = false;

	const handleScroll = () => {
		isVisible = window.scrollY > 300; // Show button after scrolling 300px
	};

	const scrollToTop = () => {
		window.scrollTo({ top: 0, behavior: 'smooth' });
	};

	onMount(() => {
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

{#if isVisible}
	<button class="scroll-top" on:click={scrollToTop} aria-label="Scroll to top">
		<img src={ArrowUpIcon} alt="Up" />
	</button>
{/if}

<style>
	.scroll-top {
		position: fixed;
		bottom: 2rem;
		right: 2rem;
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
		backdrop-filter: blur(15px);
		-webkit-backdrop-filter: blur(15px);
		border-radius: 20px;
		border: 1px solid rgba(255, 255, 255, 0.2);
		width: clamp(4rem, 5vw, 4.5rem);
		height: clamp(4rem, 5vw, 4.5rem);
		display: flex;
		align-items: center;
		justify-content: center;
		cursor: pointer;
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);
		transition:
			transform 0.3s,
			box-shadow 0.3s;
		z-index: 1000;
	}

	.scroll-top img {
		width: 50%;
		height: 50%;
		object-fit: contain;
	}

	.scroll-top:hover {
		transform: translateY(-3px);
		box-shadow:
			0 12px 36px rgba(27, 120, 222, 0.2),
			0 0 30px rgba(27, 120, 222, 0.3);
	}
</style>
