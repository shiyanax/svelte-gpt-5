<script>
	// Smooth scroll to your Early Access form or section
	function scrollToEarlyAccess() {
		document.getElementById('early-access-form')?.scrollIntoView({ behavior: 'smooth' });
	}
</script>

<section class="early-access-section breathing">
	<div class="early-access-content">
		<p class="pretitle">Request Early Access</p>
		<h2 class="title">Be the first to explore the endless possibilities</h2>
		<p class="subtitle">Sign up now to get early access and exclusive updates.</p>
		<button class="cta-btn" on:click={scrollToEarlyAccess}>Get Early Access</button>
	</div>
</section>

<style>
	/* Early Access Section */
	.early-access-section {
		padding: clamp(4rem, 8vw, 13.6rem);
		margin-left: clamp(4rem, 8vw, 13.6rem);
		margin-right: clamp(4rem, 8vw, 13.6rem);
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
		backdrop-filter: blur(15px);
		-webkit-backdrop-filter: blur(15px);
		border-radius: 20px;
		border: 1px solid rgba(255, 255, 255, 0.2);
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		color: #81afdd;
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease;
	}

	/* Breathing Animation */
	.breathing {
		animation: breathe 4s ease-in-out infinite;
	}

	@keyframes breathe {
		0%,
		100% {
			transform: scale(1);
		}
		50% {
			transform: scale(1.02);
		}
	}

	.early-access-content {
		display: flex;
		flex-direction: column;
		gap: clamp(1.5rem, 2vw, 2.5rem);
		max-width: 800px;
	}

	.pretitle {
		font-size: clamp(1.6rem, 2vw, 2rem);
		font-weight: 500;
		text-transform: uppercase;
		letter-spacing: 1px;
		color: #81afdd;
	}

	.title {
		font-size: clamp(2.4rem, 5vw, 3.2rem);
		font-weight: 700;
		line-height: 1.2;
		background: linear-gradient(to right, #f49867, #ae67fa);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.subtitle {
		font-size: clamp(1.6rem, 2vw, 2rem);
		line-height: 1.5;
		color: rgba(129, 175, 221, 0.9);
	}

	/* CTA Button - matches blog card style */
	.cta-btn {
		padding: clamp(1.6rem, 2vw, 2rem) clamp(2.4rem, 4vw, 3.6rem);
		font-size: clamp(1.6rem, 2vw, 2rem);
		font-weight: 700;
		color: #81afdd;
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
		backdrop-filter: blur(15px);
		-webkit-backdrop-filter: blur(15px);
		border-radius: 10px;
		border: 1px solid rgba(255, 255, 255, 0.2);
		cursor: pointer;
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease,
			filter 0.3s ease;
	}

	.cta-btn:hover {
		transform: translateY(-3px);
		box-shadow:
			0 12px 36px rgba(27, 120, 222, 0.2),
			0 0 30px rgba(27, 120, 222, 0.3);
		filter: brightness(1.1);
	}

	/* Responsive */
	@media (max-width: 1000px) {
		.early-access-section {
			padding: clamp(3rem, 6vw, 8rem);
			margin: clamp(3rem, 6vw, 8rem);
		}
	}
</style>
