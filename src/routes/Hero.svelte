<script lang="ts">
	import heroSection from "$lib/cms_data/hero-section.json"
</script>

<section>
	<article>
		<h1>
			{heroSection.title}
		</h1>
		<div class="cta">
			<p>{heroSection.subtitle}</p>
			<div class="signup">
				<input type="email" placeholder="Enter your email" />
				<button class="button button--solid">Sign Up</button>
			</div>
		</div>
	</article>
</section>

<style>
	section {
		background: var(--red);
		display: flex;
		justify-content: center;
		padding: 77px 20px;
	}

	article {
		display: flex;

		flex-direction: column;

		h1,
		.cta {
			flex: 1;
		}

		@media (min-width: 925px) {
			flex-direction: row;
			max-width: 925px;
		}
	}

	h1 {
		color: #fff;
		font-family: "PP Fuji";
		font-size: 55px;
		font-style: normal;
		font-weight: 700;
		line-height: 50px;
		letter-spacing: -0.275px;
		padding-bottom: 1rem;
	}

	.cta {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		justify-content: space-between;

		p {
			color: #fff;
			font-family: "Sofia Pro";
			font-size: 20px;
			font-style: normal;
			font-weight: 600;
			line-height: 120%; /* 24px */
			letter-spacing: -0.1px;
		}

		.signup {
			display: flex;
			gap: 12px;

			input {
				display: flex;
				height: 48px;
				padding: 12px 16px;
				align-items: center;
				gap: 8px;
				align-self: stretch;
				width: 100%;

				border-radius: 12px;
				border: 2px solid var(--Triathacore-Black, #23242a);
				background: #fff;
			}

			.button {
				flex-shrink: 0;
			}
		}
	}
</style>
