<script>
	import pic_1 from '$assets/pic-1.jpeg';
	import pic_2 from '$assets/pic-2.jpeg';
	import pic_3 from '$assets/pic-3.jpeg';
	import GradientTitle from '$components/GradientTitle.svelte';

	// Smooth scroll to blog section
	function scrollToBlog() {
		document.querySelector('.blog-grid')?.scrollIntoView({ behavior: 'smooth' });
	}
</script>

<section class="blog-section">
	<GradientTitle
		text="A lot is happening, We are blogging about it."
		minSize="2.4rem"
		vwSize="6vw"
		maxSize="3.2rem"
		weight={700}
		gradient="linear-gradient(to right,#f49867, #ae67fa)"
	/>

	<div class="blog-grid">
		<div class="blog-card">
			<img src={pic_1} alt="Blog 1" class="blog-img" />
			<div class="blog-text">
				<p>
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Explicabo at natus amet a id
					hic, dolorum veniam reiciendis et expedita similique soluta! Unde illo sapiente quibusdam
					quisquam pariatur, veniam delectus!
				</p>
			</div>
		</div>

		<div class="blog-card">
			<img src={pic_2} alt="Blog 2" class="blog-img" />
			<div class="blog-text">
				<p>
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Explicabo at natus amet a id
					hic, dolorum veniam reiciendis et expedita similique soluta! Unde illo sapiente quibusdam
					quisquam pariatur, veniam delectus!
				</p>
			</div>
		</div>

		<div class="blog-card">
			<img src={pic_3} alt="Blog 3" class="blog-img" />
			<div class="blog-text">
				<p>
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Explicabo at natus amet a id
					hic, dolorum veniam reiciendis et expedita similique soluta! Unde illo sapiente quibusdam
					quisquam pariatur, veniam delectus!
				</p>
			</div>
		</div>
	</div>
	<button class="scroll-btn" on:click={scrollToBlog}> Go to Blog </button>
</section>

<style>
	.blog-section {
		padding: clamp(4rem, 8vw, 13.6rem);
		display: flex;
		flex-direction: column;
		gap: clamp(2rem, 4vw, 4rem);
		box-sizing: border-box;
	}

	.scroll-btn {
		padding: clamp(1.6rem, 2vw, 2.6rem) clamp(1.6rem, 2vw, 3.4rem);
		font-size: clamp(1.6rem, 1.5vw, 2rem);
		font-weight: 700;
		color: #81afdd; /* same as card text */
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
		width: fit-content;
	}

	.scroll-btn:hover {
		transform: translateY(-3px);
		box-shadow:
			0 12px 36px rgba(27, 120, 222, 0.2),
			0 0 30px rgba(27, 120, 222, 0.3);
		filter: brightness(1.1);
	}

	/* Blog Grid */
	.blog-grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: clamp(2rem, 3vw, 3rem);
	}

	/* Glassy Glow Cards */
	.blog-card {
		position: relative;
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
		backdrop-filter: blur(15px);
		-webkit-backdrop-filter: blur(15px);
		border-radius: 20px;
		border: 1px solid rgba(255, 255, 255, 0.2);
		overflow: hidden;
		display: flex;
		flex-direction: column;
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease;
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);
		cursor: pointer; /* <-- Makes cards clickable */
	}

	.blog-card:hover {
		transform: translateY(-5px);
		box-shadow:
			0 12px 36px rgba(27, 120, 222, 0.2),
			0 0 30px rgba(27, 120, 222, 0.3);
	}

	/* Blog Images Full Width */
	.blog-img {
		width: 100%;
		display: block;
		height: auto;
		object-fit: cover;
		border-radius: 20px 20px 0 0;
		transition: transform 0.3s ease;
	}

	.blog-card:hover .blog-img {
		transform: scale(1.03);
	}

	/* Blog Text with padding */
	.blog-text {
		padding: clamp(1rem, 2vw, 1.5rem);
		color: #81afdd;
		font-size: clamp(1.6rem, 2vw, 2rem);
		line-height: 1.5;
	}

	/* Mobile Responsive */
	@media (max-width: 1000px) {
		.blog-grid {
			grid-template-columns: 1fr;
		}
		.scroll-btn {
			align-self: center;
		}
	}
</style>
