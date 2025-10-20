<script lang="ts">
	let {
		title,
		subtitle,
		images
	}: {
		title: string
		subtitle: string
		images: { image: string }[]
	} = $props()
</script>

<section>
	<article>
		<h2>{title}</h2>
		<p>{subtitle}</p>
		<div class="image-grid">
			{#each images as { image }, index (index)}
				<img src={image} alt={index + ""} />
			{/each}
		</div>
	</article>
</section>

<style>
	article {
		max-width: 784px;
		margin: auto;
		padding: 56px 20px;
		display: flex;
		flex-direction: column;
		gap: 47px;
	}

	h2 {
		font-family: PP Fuji;
		font-weight: 700;
		font-style: Bold;
		font-size: 40px;
		line-height: 88%;
		letter-spacing: -0.5%;
		text-align: center;
		vertical-align: middle;
	}

	p {
		font-family: "Sofia Pro";
		font-weight: 500;
		font-style: Medium;
		font-size: 18.14px;
		line-height: 160%;
		letter-spacing: 0%;
		text-align: center;
		max-width: 700px;
		white-space: pre-wrap;
	}

	.image-grid {
		display: grid;

		gap: 20px;
		grid-template-columns: 1fr 1fr;

		img {
			border-radius: 20px;
			aspect-ratio: 1;
			min-height: 0;
			object-fit: cover;
		}

		@media (min-width: 500px) {
			grid-template-columns: 1fr 1fr 1fr;
			gap: 32px;
		}

		@media (min-width: 700px) {
			grid-template-columns: 1fr 1fr 1fr 1fr;
			gap: 47px;
		}
	}
</style>
