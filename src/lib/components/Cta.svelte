<section class="cta-section breathing-section glowing-section">
	<div class="cta-content">
		<p class="cta-pretitle">Request Early Access to Get Started</p>
		<h3 class="cta-title">Register today & start exploring the endless possibilities.</h3>
	</div>
	<button class="cta-btn">Get Started</button>
</section>

<style>
	/* Main CTA Section */
	.cta-section {
		background: linear-gradient(to right, #ae67fa, #f49867);
		border-radius: 20px;
		padding: clamp(4rem, 8vw, 13.6rem); /* internal padding */
		margin-left: clamp(4rem, 8vw, 13.6rem); /* outer spacing like other components */
		margin-right: clamp(4rem, 8vw, 13.6rem); /* outer spacing like other components */
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: clamp(2rem, 4vw, 4rem);
		color: #000;
		font-size: 1.6rem;
		box-sizing: border-box;
		flex-wrap: wrap;
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease;
	}

	/* Breathing animation for entire section */
	.breathing-section {
		animation: breathe-section 4s ease-in-out infinite;
	}

	@keyframes breathe-section {
		0%,
		100% {
			transform: scale(1);
			box-shadow: 0 0 40px rgba(255, 150, 100, 0.4);
		}
		50% {
			transform: scale(1.02); /* subtle scale for pulse effect */
			box-shadow: 0 0 60px rgba(255, 150, 100, 0.6);
		}
	}

	/* Glow overlay */
	.glowing-section {
		box-shadow: 0 0 40px rgba(255, 150, 100, 0.4);
	}

	/* Text Content */
	.cta-content {
		display: flex;
		flex-direction: column;
		gap: clamp(1rem, 2vw, 2rem);
	}

	.cta-pretitle {
		font-size: clamp(1.4rem, 2.2vw, 1.8rem);
		font-weight: 500;
	}

	.cta-title {
		font-size: clamp(2rem, 3vw, 2.6rem);
		font-weight: 700;
		line-height: 1.4;
		text-shadow: 0 2px 6px rgba(0, 0, 0, 0.2); /* subtle text pop */
	}

	/* Button */
	.cta-btn {
		background: #000;
		color: #fff;
		padding: clamp(1rem, 2vw, 1.6rem) clamp(2rem, 4vw, 4rem);
		border: none;
		border-radius: 100px;
		font-size: clamp(1.6rem, 2.5vw, 2rem);
		font-weight: 600;
		cursor: pointer;
		transition:
			transform 0.3s ease,
			filter 0.3s ease,
			box-shadow 0.3s ease;
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
	}

	.cta-btn:hover {
		transform: translateY(-2px) scale(1.05);
		filter: brightness(1.1);
		box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
	}

	/* Mobile Responsive */
	@media (max-width: 1000px) {
		.cta-section {
			flex-direction: column;
			text-align: center;
			padding: clamp(3rem, 6vw, 8rem);
			margin: clamp(3rem, 6vw, 8rem); /* mobile spacing */
			gap: clamp(2rem, 4vw, 3rem);
		}

		.cta-btn {
			width: 100%;
		}
	}
</style>
