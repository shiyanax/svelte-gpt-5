<script>
	import featureImage from '$assets/featureImage.png';
	import GradientTitle from '$components/GradientTitle.svelte';
</script>

<section class="feature-section">
	<figure class="feature-image">
		<img src={featureImage} alt="woman with vr" />
	</figure>
	<div class="feature-content">
		<p class="pre-title">Request Early Access to Get Started</p>
		<GradientTitle
			text="Step Into the Future of Experience"
			minSize="2.4rem"
			vwSize="5vw"
			maxSize="3.2rem"
			weight={700}
			gradient="linear-gradient(to right,#ae67fa,#f49867)"
		/>
		<p class="feature-text">
			Yet bed any for travelling assistance indulgence unpleasing. Not thoughts all exercise
			blessing. Indulgence way everything joy alteration boisterous the attachment. Party we years
			to order allow asked of.
		</p>
		<a href="#" class="explore-btn">
			<GradientTitle
				text="Explore More"
				minSize="2rem"
				vwSize="2rem"
				maxSize="2rem"
				weight={400}
				gradient="linear-gradient(to right,#f49867,#ae67fa)"
				className="breathing"
			/>
		</a>
	</div>
</section>

<style>
	.feature-section {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: clamp(3rem, 5vw, 6rem);
		align-items: center;
		padding: clamp(4rem, 8vw, 13.6rem);
		color: #fff;
		box-sizing: border-box;
	}

	.feature-image img {
		width: 100%;
		height: auto;
		object-fit: cover;
	}

	.feature-content {
		display: flex;
		flex-direction: column;
		gap: clamp(2rem, 4vw, 3rem);
	}

	.pre-title {
		font-size: clamp(1.6rem, 2.5vw, 1.8rem);
		color: #71e5ff;
		font-weight: 500;
	}

	.feature-text {
		font-size: clamp(1.6rem, 2vw, 1.9rem);
		line-height: 1.6;
		color: #81afdd;
	}

	.explore-btn {
		display: inline-block;
		margin-top: 1.6rem;
		cursor: pointer;
		margin-left: 5%;
	}

	@media (max-width: 1000px) {
		.feature-section {
			grid-template-columns: 1fr;
			padding: clamp(3rem, 5vw, 5rem);
			gap: clamp(2rem, 4vw, 3rem);
		}

		.feature-content {
			align-items: flex-start;
			text-align: left;
		}
	}
</style>
