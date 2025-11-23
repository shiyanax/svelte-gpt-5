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

	const usefulLinks = [
		{ name: 'Home', url: '#home' },
		{ name: 'Blog', url: '#blog' },
		{ name: 'About', url: '#about' },
		{ name: 'Contact', url: '#contact' }
	];

	const legalLinks = [
		{ name: 'Privacy Policy', url: '#privacy' },
		{ name: 'Terms of Use', url: '#terms' },
		{ name: 'Support', url: '#support' }
	];
</script>

<footer class="footer-section">
	<div class="footer-grid">
		<div class="footer-brand">
			<h2 class="footer-logo">Gpt-5</h2>
			<p>Building innovative experiences for you.</p>
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

		<div class="footer-links">
			<h3>Useful Links</h3>
			<ul>
				{#each usefulLinks as link}
					<li><a href={link.url}>{link.name}</a></li>
				{/each}
			</ul>
		</div>

		<div class="footer-legal">
			<h3>Legal & Support</h3>
			<ul>
				{#each legalLinks as link}
					<li><a href={link.url}>{link.name}</a></li>
				{/each}
			</ul>
		</div>
	</div>

	<hr class="footer-divider" />
	<p class="footer-copy">© {new Date().getFullYear()} Gpt-5. All rights reserved.</p>
</footer>

<style>
	.footer-section {
		margin-top: 8rem;
		padding: 4rem 2rem;
		background-color: #0d1117;
		color: #cfd8e3;
		font-family: 'Inter', sans-serif;
	}

	.footer-grid {
		padding-top: 4rem;
		padding-bottom: 4rem;
		display: grid;
		grid-template-columns: 2fr 1fr 1fr;
		gap: 3rem;
		align-items: start;
		max-width: 1200px;
		margin: 0 auto;
	}

	.footer-logo {
		font-size: 2.4rem;
		font-weight: 700;
		background: linear-gradient(to right, #f49867, #ae67fa);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		margin-bottom: 1rem;
	}

	.footer-brand p {
		font-size: 1.5rem;
		margin-bottom: 1.5rem;
		line-height: 1.5;
	}

	.footer-links h3,
	.footer-legal h3 {
		font-size: 1.6rem;
		margin-bottom: 1rem;
		color: #81afdd;
	}

	.footer-links ul,
	.footer-legal ul {
		list-style: none;
		padding: 0;
		display: flex;
		flex-direction: column;
		gap: 0.6rem;
	}

	.footer-links a,
	.footer-legal a {
		color: #cfd8e3;
		text-decoration: none;
		font-size: 1.5rem;
		transition: color 0.3s;
	}

	.footer-links a:hover,
	.footer-legal a:hover {
		color: #f49867;
	}

	.social-icons {
		display: flex;
		gap: 1rem;
		margin-top: 1rem;
	}

	.icon-wrapper {
		width: 40px;
		height: 40px;
		display: flex;
		align-items: center;
		justify-content: center;
		border-radius: 50%;
		background: #1b78de22;
		transition: all 0.3s ease;
	}

	.icon-wrapper img {
		width: 60%;
		height: 60%;
		object-fit: contain;
	}

	.icon-wrapper:hover {
		transform: scale(1.1);
		background: #1b78de44;
		box-shadow: 0 4px 12px rgba(27, 120, 222, 0.3);
	}

	.footer-divider {
		border: none;
		border-top: 1px solid #1b78de22;
		margin: 2rem 0;
	}

	.footer-copy {
		text-align: center; /* centered copyright */
		color: #8b9bb4;
		font-size: 1.4rem;
		margin-bottom: 0;
	}

	/* Mobile */
	@media (max-width: 768px) {
		.footer-grid {
			grid-template-columns: 1fr;
			gap: 2rem;
		}

		.footer-brand,
		.footer-links,
		.footer-legal {
			text-align: left; /* everything left-aligned */
		}
	}
</style>
