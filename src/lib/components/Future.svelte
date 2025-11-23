<script>
	import GradientTitle from '$components/GradientTitle.svelte';
	import TitleWithLine from '$components/TitleWithLine.svelte';
</script>

<section class="future">
	<div class="col-2">
		<div class="future-title">
			<GradientTitle
				text="The Future is Now and You Just Need To Realize It. Step into Future Today & Make it Happen."
				minSize="2rem"
				vwSize="6vw"
				maxSize="7.6rem"
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
		<div class="future-content">
			<div class="items">
				<TitleWithLine
					title="Improving end distrusts instantly"
					fontSize="clamp(1.6rem, 5vw, 1.8rem)"
				/>
				<p class="title-content">
					We so opinion friends me message as delight. Whole front do of plate heard oh ought.
				</p>
			</div>
			<div class="items">
				<TitleWithLine title="Become the tended active" fontSize="clamp(1.6rem, 5vw, 1.8rem)" />
				<p class="title-content">
					We so opinion friends me message as delight. Whole front do of plate heard oh ought.
				</p>
			</div>
			<div class="items">
				<TitleWithLine title="Message or am nothing" fontSize="clamp(1.6rem, 5vw, 1.8rem)" />
				<p class="title-content">
					We so opinion friends me message as delight. Whole front do of plate heard oh ought.
				</p>
			</div>
			<div class="items">
				<TitleWithLine title="Really boy law county" fontSize="clamp(1.6rem, 5vw, 1.8rem)" />
				<p class="title-content">
					We so opinion friends me message as delight. Whole front do of plate heard oh ought.
				</p>
			</div>
		</div>
	</div>
</section>

<style>
	.future {
		padding: clamp(4rem, 8vw, 13.6rem);
		padding-top: clamp(4rem, 8vw, 10rem); /* more room from previous section */
		display: flex;
		flex-direction: column;
		gap: clamp(4rem, 6vw, 8rem); /* more breathing space */
		box-sizing: border-box;
		color: #fff;
	}

	/* Desktop ≥ 1000px */
	.col-2 {
		display: grid;
		grid-template-columns: 45% 55%; /* more room for large title */
		gap: clamp(4rem, 5vw, 6rem); /* more space between columns */
	}

	.future-title {
		display: flex;
		flex-direction: column;
		gap: clamp(2.5rem, 4vw, 4.5rem); /* bigger vertical spacing */
		align-items: flex-start;
	}

	.explore-btn {
		margin-left: 0.8rem;
		cursor: pointer;
		display: inline-block;
	}

	.future-content {
		display: grid;
		grid-template-rows: repeat(4, auto);
		gap: clamp(3rem, 4vw, 5rem); /* more room between items */
	}

	.items {
		display: flex;
		flex-direction: column;
		gap: clamp(2.5rem, 4vw, 4rem); /* more breathing space inside each card */
		margin-bottom: 2rem;
	}

	.title-content {
		font-size: clamp(1.8rem, 2vw, 2rem);
		line-height: 1.5;
		color: #81afdd;
		line-height: 1.6; /* slightly improved readability */
		margin: 0;
	}

	/* Mobile ≤ 1000px */
	@media (max-width: 1000px) {
		.future {
			padding: clamp(3rem, 6vw, 7rem);
			gap: clamp(3rem, 5vw, 5rem);
		}

		.col-2 {
			grid-template-columns: 1fr;
			gap: clamp(3rem, 5vw, 5rem);
		}

		.future-title {
			gap: clamp(2rem, 4vw, 3.5rem);
			margin-bottom: 4rem;
		}

		.items {
			gap: 2rem;
			margin-bottom: 2rem;
		}

		.future-content {
			gap: clamp(3rem, 5vw, 4.5rem);
		}

		.title-content {
			font-size: clamp(1.6rem, 3vw, 1.8rem);
		}
	}
</style>
