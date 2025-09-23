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
			<form
				class="signup"
				method="post"
				action="https://gmail.us7.list-manage.com/subscribe/post?u=ada22d22957f9b0b5146cb213&amp;id=b223cf557d&amp;f_id=0026c0e1f0"
				name="mc-embedded-subscribe-form"
				target="_blank"
			>
				<input type="email" name="EMAIL" required placeholder="Enter your email" />
				<input
					class="visually-hidden"
					type="text"
					name="b_ada22d22957f9b0b5146cb213_b223cf557d"
					tabindex="-1"
					value=""
				/>
				<button class="button button--solid" type="submit">Sign Up</button>
			</form>
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

	.visually-hidden {
		position: absolute;
		width: 1px;
		height: 1px;
		padding: 0;
		margin: -1px;
		overflow: hidden;
		clip: rect(0, 0, 0, 0);
		white-space: nowrap; /* prevent line breaks */
		border: 0;

		position: absolute;
		bottom: 0;
		right: 0;
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
