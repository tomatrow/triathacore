<script lang="ts">
	import communityImagePlaceholder from "$lib/assets/community-image-placeholder.jpg"
</script>

<section>
	<article>
		<h2>Creating a Brighter Community for All</h2>

		<div>
			<p>
				"This is more than a team. It’s a family. Triathacore gave us a place to be active together
				and truly belong. It’s made a world of difference for our son."
			</p>
			<p>－ Laura B., Parent & Runner</p>
		</div>

		<div class="image-grid">
			{#each Array.from({ length: 8 }) as _, index (index)}
				<img src={communityImagePlaceholder} alt={_ + ""} />
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
	}

	.image-grid {
		display: grid;
		gap: 47px;
		grid-template-columns: 1fr 1fr 1fr 1fr;

		img {
			border-radius: 20px;
			aspect-ratio: 1;
			min-height: 0;
			object-fit: cover;
		}
	}
</style>
