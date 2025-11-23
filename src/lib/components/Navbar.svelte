<script>
	let isOpen = false;
</script>

<nav class="nav">
	<div class="container">
		<!-- Logo -->
		<div class="logo">GPT-5</div>

		<!-- Desktop Links -->
		<ul class="nav-links">
			<li><a href="/">Home</a></li>
			<li><a href="/what-is-gpt">What is GPT?</a></li>
			<li><a href="/openai">OpenAI</a></li>
			<li><a href="/case-studies">Case Studies</a></li>
			<li><a href="/library">Library</a></li>
		</ul>

		<!-- Desktop Buttons -->
		<div class="auth">
			<a class="signin" href="/sign-in">Sign In</a>
			<a class="signup" href="/sign-up">Sign Up</a>
		</div>

		<!-- Mobile Hamburger -->
		<button class="mobile-btn" on:click={() => (isOpen = !isOpen)}>
			{#if isOpen}
				✕
			{:else}
				☰
			{/if}
		</button>
	</div>

	<!-- Mobile Menu -->
	<div class="mobile-menu glass" class:open={isOpen}>
		<a href="/">Home</a>
		<a href="/what-is-gpt">What is GPT?</a>
		<a href="/openai">OpenAI</a>
		<a href="/case-studies">Case Studies</a>
		<a href="/library">Library</a>

		<div class="mobile-login">
			<a href="/sign-in" class="signin mobile-auth">Sign In</a>
			<a href="/sign-up" class="signup mobile-auth">Sign Up</a>
		</div>
	</div>
</nav>

<style>
	/* NAV WRAPPER - Glassmorphic Gradient Blur */
	.nav {
		width: 100%;
		background: linear-gradient(rgba(4, 12, 24, 0.35), rgba(4, 12, 24, 0.55)); /* soft gradient */
		backdrop-filter: blur(25px) saturate(150%); /* strong blur glass */
		-webkit-backdrop-filter: blur(25px) saturate(150%);
		position: sticky;
		top: 0;
		z-index: 1000;
		border-bottom: 1px solid rgba(255, 255, 255, 0.1); /* subtle glass line */
	}

	/* MAX WIDTH CONTAINER */
	.container {
		max-width: 120rem;
		margin: 0 auto;
		padding: 1.6rem;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.logo {
		font-size: 2.4rem;
		font-weight: 700;
		text-transform: uppercase;
		color: #fff;
	}

	/* DESKTOP NAV LINKS */
	.nav-links {
		display: flex;
		gap: 3rem;
		list-style: none;
	}
	.nav-links a {
		text-decoration: none;
		color: #fff;
		font-size: 1.8rem;
		font-weight: 500;
		cursor: pointer;
	}

	/* DESKTOP AUTH BUTTONS */
	.auth {
		display: flex;
		gap: 2rem;
		align-items: center;
	}
	.signin {
		color: #fff;
		font-size: 1.8rem;
		font-weight: 500;
		text-decoration: none;
		transition: 0.4s ease;
	}
	.signup {
		background: #ff4820;
		color: #fff !important;
		padding: 1.2rem 3rem;
		border-radius: 10px;
		font-size: 1.8rem;
		font-weight: 600;
		text-decoration: none;
		transition: 0.4s ease;
	}
	.signup:hover,
	.signin:hover {
		filter: brightness(80%);
	}

	/* MOBILE HAMBURGER */
	.mobile-btn {
		display: none;
		font-size: 3rem;
		background: none;
		border: none;
		cursor: pointer;
		color: #fff;
		z-index: 1100;
	}

	/* MOBILE MENU - Glass Dropdown */
	.mobile-menu {
		display: flex;
		flex-direction: column;
		gap: 2rem;
		padding: 2rem;
		position: absolute;
		top: 7rem;
		left: 50%;
		transform: translateX(-50%) translateY(-20px) scale(0.95);
		width: 90%;
		background: rgba(4, 12, 24, 0.7);
		backdrop-filter: blur(20px) saturate(160%);
		-webkit-backdrop-filter: blur(20px) saturate(160%);
		border-radius: 20px;
		box-shadow:
			0px 30px 50px rgba(0, 0, 0, 0.35),
			0px 0px 25px rgba(80, 160, 255, 0.2);
		opacity: 0;
		pointer-events: none;
		transition:
			transform 0.4s ease,
			opacity 0.4s ease,
			box-shadow 0.4s ease;
		z-index: 1050;
	}

	.mobile-menu.open {
		opacity: 1;
		transform: translateX(-50%) translateY(10px) scale(1);
		pointer-events: auto;
	}

	.mobile-menu a {
		color: #fff;
		font-size: 2rem;
		text-decoration: none;
		font-weight: 500;
		transition: 0.4s ease;
	}
	.mobile-menu > a:hover {
		transform: translateX(5%);
	}

	.mobile-login {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 1.6rem;
		margin-top: 1rem;
	}

	.mobile-login .signin {
		color: #ff4820;
		background: #fff;
		border-radius: 10px;
	}

	.mobile-auth {
		text-align: center;
		padding: 1.6rem;
		font-weight: 600;
		font-size: 1.8rem;
	}

	/* RESPONSIVE - Mobile */
	@media (max-width: 1000px) {
		.nav-links,
		.auth {
			display: none;
		}

		.mobile-btn {
			display: block;
		}
	}
</style>
