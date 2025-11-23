<script>
	import GradientTitle from '$components/GradientTitle.svelte';
	import TitleWithLine from '$components/TitleWithLine.svelte';
</script>

<section class="about">
	<div class="intro">
		<TitleWithLine title="What is GPT?" />
		<p class="title-content">
			We value your opinions and insights. Every message and interaction matters to us. GPT-5 helps
			bridge understanding, turning complex ideas into clear, actionable content. Its capabilities
			extend to generating creative solutions, providing thoughtful responses, and supporting
			decision-making. With GPT-5, every conversation becomes more meaningful, and every interaction
			more engaging.
		</p>
	</div>
	<div class="detail-heading">
		<GradientTitle
			text="The possibilities are beyond your imagination"
			minSize="2rem"
			vwSize="6vw"
			maxSize="3.4rem"
			weight={700}
			gradient="linear-gradient(to right,#ae67fa,#f49867)"
		/>

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
	<div class="col-3">
		<div class="items">
			<TitleWithLine title="Chatbots" />
			<p class="title-content">
				We so opinion friends me message as delight. Whole front do of plate heard oh ought.
			</p>
		</div>
		<div class="items">
			<TitleWithLine title="Knowledgeable" />
			<p class="title-content">
				We so opinion friends me message as delight. Whole front do of plate heard oh ought.
			</p>
		</div>
		<div class="items">
			<TitleWithLine title="Education" />
			<p class="title-content">
				We so opinion friends me message as delight. Whole front do of plate heard oh ought.
			</p>
		</div>
	</div>
</section>

<style>
	.col-3 {
		margin-top: 2rem;
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 8rem;
	}
	.items {
		display: flex;
		flex-direction: column;
		gap: clamp(2rem, 5vw, 4rem);
	}
	.about {
		position: relative;
		background: rgba(27, 120, 222, 0.1); /* very transparent blue */
		backdrop-filter: blur(20px); /* frosted effect */
		-webkit-backdrop-filter: blur(20px); /* Safari support */
		border-radius: 20px;
		border: 1px solid rgba(255, 255, 255, 0.2); /* soft white border for glass edge */

		margin: clamp(2rem, 8vw, 13.6rem);
		padding: clamp(3rem, 8vw, 6rem);
		display: flex;
		flex-direction: column;
		gap: clamp(2rem, 4vw, 5rem);

		/* subtle glow */
		box-shadow:
			0 8px 32px rgba(27, 120, 222, 0.1),
			0 0 20px rgba(27, 120, 222, 0.2);

		/* inner highlight to enhance glass effect */
		background: linear-gradient(rgba(27, 120, 222, 0.1), rgba(27, 120, 222, 0.05));
	}

	.intro {
		display: flex;
		flex-direction: column;
		align-items: start;
		gap: clamp(2rem, 5vw, 4rem);
	}

	.title-content {
		justify-self: start;
		font-size: clamp(1.6rem, 2vw, 2rem);
		color: #81afdd;
		line-height: 1.5;
		margin: 0;
		grid-column: 2 / -1;
	}

	.detail-heading {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
		align-items: flex-start;
		margin-top: 2rem;
	}

	.explore-btn {
		margin-left: 1rem;
		cursor: pointer;
		display: inline-block;
	}

	/* RESPONSIVE */
	@media (max-width: 1000px) {
		.about {
			margin: clamp(2rem, 5vw, 6rem);
			gap: clamp(1.5rem, 4vw, 3rem);
		}

		.intro {
			gap: clamp(1.5rem, 4vw, 3rem);
		}

		.col-3 {
			grid-template-columns: 1fr;
			gap: 4rem;
		}
	}
</style>
