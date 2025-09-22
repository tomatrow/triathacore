<script lang="ts">
	import sponsorImagePlaceholder from "$lib/assets/sponsor-image-placeholder.svg"
</script>

<section>
	<article>
		<h2>Our Sponsors</h2>

		<div class="image-grid">
			{#each Array.from({ length: 10 }) as _, index (index)}
				<a href="https://redbike.agency" target="_blank">
					<img src={sponsorImagePlaceholder} alt={index + ""} />
				</a>
			{/each}
		</div>
	</article>
</section>

<style>
	section {
		padding: 56px 20px;
		background: #23242a;

		article {
			display: flex;
			flex-direction: column;
			gap: 32px;
			align-items: center;
		}
	}

	h2 {
		color: #fff;
		text-align: center;
		font-family: "PP Fuji";
		font-size: 40px;
		font-style: normal;
		font-weight: 700;
		line-height: 88%; /* 35.2px */
		letter-spacing: -0.2px;
	}

	.image-grid {
		display: grid;
		gap: 28px;
		grid-template-columns: 1fr;

		img {
			max-width: 167px;
			aspect-ratio: 1;
		}

		@media (min-width: 400px) {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}

		@media (min-width: 700px) {
			grid-template-columns: repeat(3, minmax(0, 1fr));
		}
	}
</style>
