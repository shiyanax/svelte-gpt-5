<script>
	import atlassian from '$assets/atlassian.png';
	import dropbox from '$assets/dropbox.png';
	import google from '$assets/google.png';
	import shopify from '$assets/shopify.png';
	import slack from '$assets/slack.png';
</script>

<section class="validation">
	<div class="slider">
		<div class="slide-track">
			<figure class="items"><img src={google} alt="google" /></figure>
			<figure class="items"><img src={slack} alt="slack" /></figure>
			<figure class="items"><img src={atlassian} alt="atlassian" /></figure>
			<figure class="items"><img src={dropbox} alt="dropbox" /></figure>
			<figure class="items"><img src={shopify} alt="shopify" /></figure>

			<!-- duplicate once for seamless loop -->
			<figure class="items"><img src={google} alt="google" /></figure>
			<figure class="items"><img src={slack} alt="slack" /></figure>
			<figure class="items"><img src={atlassian} alt="atlassian" /></figure>
			<figure class="items"><img src={dropbox} alt="dropbox" /></figure>
			<figure class="items"><img src={shopify} alt="shopify" /></figure>
		</div>
	</div>
</section>

<style>
	.validation {
		overflow: hidden;
		width: 100%;
		padding: 3rem 0;
	}

	.slider {
		width: 100%;
		overflow: hidden;
	}

	.slide-track {
		display: flex;
		align-items: center;
		flex-wrap: nowrap;
		width: max-content;
		animation: scroll 15s linear infinite;
	}

	.items {
		flex: 0 0 auto;
		width: 12rem;
		margin-right: 19rem; /* spacing between logos */
	}

	.items img {
		width: 100%;
		display: block;
	}

	/* Keyframes for smooth loop */
	@keyframes scroll {
		0% {
			transform: translateX(0);
		}
		100% {
			transform: translateX(-50%); /* half of the track since duplicated once */
		}
	}

	/* Responsive */
	@media (max-width: 1000px) {
		.items {
			width: 10rem;
			margin-right: 4rem;
		}
	}

	@media (max-width: 600px) {
		.items {
			width: 8rem;
			margin-right: 3rem;
		}
	}
</style>
