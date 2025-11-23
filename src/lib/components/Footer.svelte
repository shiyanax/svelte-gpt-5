<script>
	import TwitterIcon from '$lib/assets/Twitter---Streamline-Bootstrap.svg';
	import InstagramIcon from '$lib/assets/instagram-167-svgrepo-com.svg';
	import LinkedInIcon from '$lib/assets/linkedin-svgrepo-com.svg';
	import FacebookIcon from '$lib/assets/meta-svgrepo-com.svg';

	const socialLinks = [
		{ name: 'Facebook', url: 'https://facebook.com', icon: FacebookIcon },
		{ name: 'Twitter', url: 'https://twitter.com', icon: TwitterIcon },
		{ name: 'Instagram', url: 'https://instagram.com', icon: InstagramIcon },
		{ name: 'LinkedIn', url: 'https://linkedin.com', icon: LinkedInIcon }
	];

	const legalLinks = [
		{ name: 'Privacy Policy', url: '#privacy' },
		{ name: 'Terms of Use', url: '#terms' },
		{ name: 'Contact', url: '#contact' }
	];
</script>

<footer class="footer-section">
	<div class="footer-container">
		<div class="footer-brand">
			<h2 class="footer-logo">Gpt-5</h2>
			<p>Building innovative experiences for you.</p>
		</div>

		<div class="footer-links">
			<h3>Useful Links</h3>
			<ul>
				<li><a href="#home">Home</a></li>
				<li><a href="#blog">Blog</a></li>
				<li><a href="#about">About</a></li>
				<li><a href="#contact">Contact</a></li>
			</ul>
		</div>

		<div class="footer-legal">
			<h3>Legal & Contact</h3>
			<ul>
				{#each legalLinks as link}
					<li><a href={link.url}>{link.name}</a></li>
				{/each}
			</ul>
		</div>

		<div class="footer-social">
			<h3>Follow Us</h3>
			<div class="social-icons">
				{#each socialLinks as link}
					<a href={link.url} target="_blank" rel="noopener noreferrer" aria-label={link.name}>
						<div class="icon-wrapper">
							<img src={link.icon} alt={link.name} />
						</div>
					</a>
				{/each}
			</div>
		</div>
	</div>

	<p class="footer-copy">© {new Date().getFullYear()} Gpt-5. All rights reserved.</p>
</footer>

<style>
	.footer-section {
		margin-top: clamp(4rem, 8vw, 8rem);
		padding: clamp(4rem, 8vw, 8rem);
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
		backdrop-filter: blur(15px);
		-webkit-backdrop-filter: blur(15px);
		border-top: 1px solid rgba(255, 255, 255, 0.2);
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);
		color: #81afdd;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: clamp(2rem, 3vw, 3rem);
	}

	.footer-container {
		display: flex;
		justify-content: space-between;
		flex-wrap: wrap;
		width: 100%;
		max-width: 1200px;
		gap: clamp(2rem, 4vw, 4rem);
	}

	.footer-brand {
		flex: 1 1 250px;
	}

	.footer-logo {
		font-size: clamp(2rem, 4vw, 2.8rem);
		font-weight: 700;
		background: linear-gradient(to right, #f49867, #ae67fa);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		margin-bottom: 1rem;
	}

	.footer-brand p {
		font-size: clamp(1.4rem, 1.5vw, 1.6rem);
	}

	.footer-links,
	.footer-legal {
		flex: 1 1 150px;
	}

	.footer-links h3,
	.footer-legal h3 {
		font-size: clamp(1.4rem, 1.5vw, 1.6rem);
		margin-bottom: 1rem;
	}

	.footer-links ul,
	.footer-legal ul {
		list-style: none;
		padding: 0;
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
	}

	.footer-links a,
	.footer-legal a {
		color: #81afdd;
		text-decoration: none;
		font-size: clamp(1.4rem, 1.5vw, 1.6rem);
		transition: 0.3s;
	}

	.footer-links a:hover,
	.footer-legal a:hover {
		color: #f49867;
	}

	.footer-social {
		flex: 1 1 150px;
	}

	.footer-social h3 {
		font-size: clamp(1.4rem, 1.5vw, 1.6rem);
		margin-bottom: 1rem;
	}

	.social-icons {
		display: flex;
		gap: clamp(1rem, 2vw, 1.5rem);
	}

	.social-icons a {
		transition: 0.3s;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.icon-wrapper {
		width: clamp(2.5rem, 3vw, 3rem);
		height: clamp(2.5rem, 3vw, 3rem);
		display: flex;
		align-items: center;
		justify-content: center;
		border-radius: 50%;
		background: rgba(27, 120, 222, 0.1);
		backdrop-filter: blur(10px);
		-webkit-backdrop-filter: blur(10px);
		box-shadow:
			0 4px 16px rgba(27, 120, 222, 0.1),
			0 0 10px rgba(27, 120, 222, 0.15);
		transition: 0.3s;
	}

	.icon-wrapper img {
		width: 60%;
		height: 60%;
		object-fit: contain;
	}

	.social-icons a:hover .icon-wrapper {
		transform: scale(1.1);
		box-shadow:
			0 6px 20px rgba(27, 120, 222, 0.2),
			0 0 15px rgba(27, 120, 222, 0.25);
	}

	.footer-copy {
		font-size: clamp(1.4rem, 1.5vw, 1.6rem);
		color: rgba(129, 175, 221, 0.8);
		text-align: center;
		margin-top: clamp(1rem, 2vw, 2rem);
	}

	@media (max-width: 1000px) {
		.footer-container {
			flex-direction: column;
			align-items: center;
			text-align: center;
		}
	}
</style>
