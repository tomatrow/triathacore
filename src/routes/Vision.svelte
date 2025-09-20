<script lang="ts">
	import vision from "$lib/assets/vision.png"
</script>

<section>
	<div class="content">
		<article>
			<h3>Our Vision</h3>

			<h2>
				<span> An Inclusive Community </span>
				<span> For All </span>
			</h2>

			<p>
				My name is Corey. As a triathlete and a father of a young boy with autism, my passions led
				to a vision: to create a fun, safe space where athletes of all abilities can compete
				together. Triathacore was born from that love. We are walkers, runners, cyclists, and
				swimmers. We are Moms, Dads, and weekend warriors. And most importantly, we are a community
				with one goal in common: to pay it forward.
			</p>
		</article>

		<img src={vision} alt="" />
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
		max-width: 925px;
		padding: 18px 20px;
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
			display: flex;
			flex-direction: column;

			color: #000;
			font-family: "PP Fuji";
			font-size: 40px;
			font-style: normal;
			font-weight: 700;
			line-height: 88%; /* 35.2px */
			letter-spacing: -0.2px;
		}
	}

	img {
		width: 383px;
	}
</style>
