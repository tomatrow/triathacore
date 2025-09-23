<script lang="ts">
	import impactSection from "$lib/cms_data/impact-section.json"
	import lightning from "$lib/assets/lightning.png"
	import heart from "$lib/assets/heart.png"
	import fist from "$lib/assets/fist.png"
</script>

<section>
	<div class="content">
		<img class="impact" src={impactSection.image} alt="" />
		<article>
			<h3>{impactSection.subtitle}</h3>
			<h2>{impactSection.title}</h2>
			<p>{impactSection.text}</p>
			<div class="row">
				<img src={lightning} alt="" />
				<p>{impactSection.bulletOne}</p>
			</div>
			<div class="row">
				<img src={heart} alt="" />
				<p>{impactSection.bulletTwo}</p>
			</div>
			<div class="row">
				<img src={fist} alt="" />
				<p>{impactSection.bulletThree}</p>
			</div>
		</article>
	</div>
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		padding: 36px 20px;
	}

	.content {
		display: flex;
		gap: 43px;
		flex-direction: column-reverse;
		align-items: center;

		@media (min-width: 925px) {
			max-width: 925px;
			flex-direction: row;
		}
	}

	article {
		display: flex;
		flex-direction: column;
		gap: 28px;

		.row {
			display: flex;
			gap: 12px;
			align-items: center;

			img {
				max-width: 26px;
			}
		}
	}

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

	p {
		color: #000;
		font-feature-settings:
			"liga" off,
			"clig" off;
		font-family: Sofia Pro;
		font-size: 16px;
		font-style: normal;
		font-weight: 500;
		line-height: 160%; /* 25.6px */
	}

	img.impact {
		width: 100%;
		max-width: 334px;
		flex-shrink: 0;
	}
</style>
