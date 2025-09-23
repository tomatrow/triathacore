<script lang="ts">
	import visionSection from "$lib/cms_data/vision-section.json"
</script>

<section>
	<div class="content">
		<article>
			<h3>{visionSection.subtitle}</h3>
			<h2>{visionSection.title}</h2>
			<p>{visionSection.text}</p>
		</article>
		<img src={visionSection.image} alt="" />
	</div>
</section>

<style>
	section {
		display: flex;
		justify-content: center;
	}

	.content {
		display: flex;
		gap: 50px;
		padding: 18px 20px;
		flex-direction: column;
		align-items: center;

		@media (min-width: 925px) {
			flex-direction: row;
			max-width: 925px;
		}
	}

	article {
		display: flex;
		flex-direction: column;
		gap: 28px;

		h3 {
			color: #ec4139;
			font-family: "PP Fuji";
			font-size: 18px;
			font-style: normal;
			font-weight: 700;
			line-height: 88%; /* 15.84px */
			letter-spacing: -0.09px;
		}

		h2 {
			color: #000;
			font-family: "PP Fuji";
			font-size: 40px;
			font-style: normal;
			font-weight: 700;
			line-height: 40px; /* 35.2px */
			letter-spacing: -0.2px;
			white-space: pre;
		}
	}

	img {
		width: 100%;
		max-width: 383px;
	}
</style>
