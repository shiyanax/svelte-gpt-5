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

	const contactDetails = {
		address: '123 AI Street, Tech City, Maldives',
		email: 'info@gpt5.com',
		phone: '+960 123-4567'
	};
</script>

<footer class="footer-section">
	<div class="footer-grid">
		<div class="footer-brand">
			<h2 class="footer-logo">Gpt-5</h2>
			<p class="footer-desc">Building innovative experiences for you.</p>
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
			<p class="legal-description">Important policies and support info for our users.</p>
			<ul>
				{#each legalLinks as link}
					<li><a href={link.url}>{link.name}</a></li>
				{/each}
			</ul>
		</div>

		<div class="footer-contact">
			<h3>Contact Us</h3>
			<p class="contact-item">Address: {contactDetails.address}</p>
			<p class="contact-item">
				Email: <a href="mailto:{contactDetails.email}">{contactDetails.email}</a>
			</p>
			<p class="contact-item">
				Phone: <a href="tel:{contactDetails.phone}">{contactDetails.phone}</a>
			</p>
		</div>
	</div>

	<hr class="footer-divider" />
	<p class="footer-copy">© {new Date().getFullYear()} Gpt-5. All rights reserved.</p>
</footer>

<style>
	.footer-section {
		margin-top: 8rem;
		padding: clamp(4rem, 6vw, 6rem);
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
		backdrop-filter: blur(15px);
		-webkit-backdrop-filter: blur(15px);
		border-top: 1px solid rgba(255, 255, 255, 0.2);
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);
		color: #81afdd;
	}

	.footer-grid {
		display: grid;
		grid-template-columns: 2fr 1fr 1fr 1fr; /* 4 columns now */
		gap: clamp(2rem, 5vw, 4rem);
		max-width: 1200px;
		margin: 0 auto;
		padding-bottom: clamp(2rem, 4vw, 3rem);
		align-items: start;
	}

	.footer-logo {
		font-size: clamp(1.6rem, 2vw, 1.8rem);
		font-weight: 700;
		background: linear-gradient(to right, #f49867, #ae67fa);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		margin-bottom: clamp(1rem, 2vw, 1.5rem);
	}

	.footer-desc {
		font-size: clamp(1.6rem, 2vw, 1.8rem);
		margin-bottom: clamp(1.5rem, 2vw, 2rem);
		line-height: 1.6;
	}

	.footer-links h3,
	.footer-legal h3,
	.footer-contact h3 {
		font-size: clamp(1.6rem, 2vw, 1.8rem);
		margin-bottom: clamp(1rem, 1.5vw, 1.2rem);
		color: #81afdd;
	}

	.footer-links ul,
	.footer-legal ul {
		list-style: none;
		padding: 0;
		display: flex;
		flex-direction: column;
		gap: clamp(0.8rem, 1.2vw, 1rem);
	}

	.footer-links a,
	.footer-legal a,
	.footer-contact a {
		color: #81afdd;
		text-decoration: none;
		font-size: clamp(1.6rem, 2vw, 1.8rem);
		transition:
			color 0.3s,
			transform 0.2s;
	}

	.footer-links a:hover,
	.footer-legal a:hover,
	.footer-contact a:hover {
		color: #f49867;
		transform: translateX(3px);
	}

	.legal-description {
		font-size: clamp(1.6rem, 2vw, 1.8rem);
		margin-bottom: clamp(0.8rem, 1vw, 1rem);
		color: #81afdd;
	}

	.contact-item {
		margin-bottom: clamp(0.8rem, 1vw, 1rem);
		font-size: clamp(1.6rem, 2vw, 1.8rem);
	}

	.social-icons {
		display: flex;
		gap: clamp(1rem, 2vw, 1.5rem);
		margin-top: clamp(1rem, 1.5vw, 2rem);
	}

	.icon-wrapper {
		width: clamp(40px, 4vw, 50px);
		height: clamp(40px, 4vw, 50px);
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
		margin: clamp(2rem, 4vw, 2.5rem) 0;
	}

	.footer-copy {
		text-align: center;
		color: #81afdd;
		font-size: clamp(1.6rem, 2vw, 1.8rem);
		margin-bottom: 0;
	}

	/* Mobile */
	@media (max-width: 768px) {
		.footer-grid {
			grid-template-columns: 1fr;
			gap: clamp(2rem, 4vw, 3rem);
		}

		.footer-brand,
		.footer-links,
		.footer-legal,
		.footer-contact {
			text-align: left;
		}
	}
</style>
