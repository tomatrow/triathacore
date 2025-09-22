<script lang="ts">
	import impact from "$lib/assets/impact.png"
	import lightning from "$lib/assets/lightning.png"
	import heart from "$lib/assets/heart.png"
	import fist from "$lib/assets/fist.png"
</script>

<section>
	<div class="content">
		<img class="impact" src={impact} alt="" />

		<article>
			<h3>Our Impact</h3>

			<h2>
				<span>Racing to Pay </span>
				<span>It Forward</span>
			</h2>

			<p>
				For every race or event we participate in, we pay it forward to a local or national
				non-profit. Your participation isn’t just a workout; it’s a powerful act of community
				support. When you join us, you help us to:
			</p>

			<div class="row">
				<img src={lightning} alt="" />
				<p>Empower children by giving them a voice and a space to thrive.</p>
			</div>

			<div class="row">
				<img src={heart} alt="" />
				<p>Support local businesses and non-profits by connecting them through our events.</p>
			</div>

			<div class="row">
				<img src={fist} alt="" />
				<p>Support local businesses and non-profits by connecting them through our events.</p>
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
		max-width: 925px;
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
		line-height: 88%; /* 35.2px */
		letter-spacing: -0.2px;

		display: flex;
		flex-direction: column;
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
		max-width: 334px;
		flex-shrink: 0;
	}
</style>
