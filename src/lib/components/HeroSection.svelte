<script>
	import heroImage from '$assets/heroImage.png';
	import usersImage from '$assets/users.png';
</script>

<section class="hero-section">
	<div class="hero-container">
		<div class="hero-content">
			<h1 class="hero-title">Let’s Build Something amazing with GPT-5 OpenAI</h1>
			<p class="hero-text">
				Yet bed any for travelling assistance indulgence unpleasing. Not thoughts all exercise
				blessing. Indulgence way everything joy alteration boisterous the attachment. Party we years
				to order allow asked of.
			</p>
			<form class="hero-form">
				<input type="email" placeholder="Your Email Address" />
				<button>Get Started</button>
			</form>
			<div class="hero-users">
				<img src={usersImage} alt="users image" />
				<p>1,600 people requested access a visit in last 24 hours</p>
			</div>
		</div>
		<div class="hero-image">
			<img src={heroImage} alt="hero image" />
		</div>
	</div>
</section>

<style>
	/* HERO SECTION */
	.hero-section {
		width: 100%;
		padding: 0;
		box-sizing: border-box;
		color: #fff;
	}

	.hero-container {
		display: grid;
		grid-template-columns: 1fr 1fr;
		align-items: center;
		width: 100%;
		padding: clamp(4rem, 8vw, 13.6rem);
		gap: clamp(2rem, 3vw, 3rem);
		box-sizing: border-box;
	}

	.hero-content {
		display: flex;
		flex-direction: column;
		gap: clamp(1.5rem, 3vw, 3rem);
	}

	.hero-title {
		width: 100%;
		font-size: clamp(2.5rem, 6vw, 7rem);
		font-weight: 700;
		background: linear-gradient(to right, #ae67fa, #f49867);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		line-height: 1.1;
		word-break: break-word;
	}

	.hero-text {
		font-size: clamp(1.6rem, 2vw, 2rem);
		color: #81afdd;
		line-height: 1.5;
	}

	.hero-form {
		display: flex;
		width: 100%;
		/* max-width: clamp(30rem, 80%, 63rem); */
	}

	.hero-form input[type='email'] {
		flex-grow: 1;
		padding: clamp(1.6rem, 2vw, 2.6rem) clamp(1rem, 2vw, 3.4rem);
		border: none;
		border-top-left-radius: 10px;
		border-bottom-left-radius: 10px;
		background-color: #052d56;
		color: #fff;
		font-size: clamp(1.6rem, 1.5vw, 2rem);
	}

	.hero-form input::placeholder {
		color: #3d6184;
		font-weight: 200;
	}

	.hero-form button {
		padding: clamp(1.6rem, 2vw, 2.6rem) clamp(1.6rem, 2vw, 3.4rem);
		font-size: clamp(1.6rem, 1.5vw, 2rem);
		font-weight: 700;
		color: #fff;
		background-color: #ff4820;
		border: none;
		border-top-right-radius: 10px;
		border-bottom-right-radius: 10px;
		cursor: pointer;
		transition: 0.4s ease;
	}

	/* Darken button by 10% on hover */
	.hero-form button:hover {
		filter: brightness(80%);
	}

	@keyframes breathe {
		0% {
			transform: scale(1);
		}
		50% {
			transform: scale(1.05);
		}
		100% {
			transform: scale(1);
		}
	}

	.hero-image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		border-radius: clamp(0, 1vw, 10px);
		display: block;
		animation: breathe 6s ease-in-out infinite;
		transform-origin: center center;
	}

	.hero-users {
		display: flex;
		align-items: center;
		gap: 1rem;
		margin-top: 2rem;
	}

	.hero-users img {
		height: 3.8rem;
	}

	.hero-users p {
		font-size: clamp(1.2rem, 2vw, 1.4rem);
	}

	/* RESPONSIVE */
	@media (max-width: 1000px) {
		.hero-title {
			font-size: clamp(2rem, 10vw, 4.5rem);
			line-height: 1.2;
		}

		.hero-container {
			grid-template-columns: 1fr;
			padding: clamp(2rem, 5vw, 6rem);
			gap: clamp(2rem, 4vw, 3rem);
		}

		.hero-image {
			order: -1;
			margin-bottom: 2rem;
		}

		.hero-form {
			flex-direction: column;
			width: 100%;
			gap: 1.5rem;
		}

		.hero-form input,
		.hero-form button {
			width: 100%;
			border-radius: 10px;
		}

		.hero-users {
			flex-direction: column;
			align-items: flex-start;
			margin-top: clamp(1.5rem, 3vw, 2rem);
		}
	}
</style>
