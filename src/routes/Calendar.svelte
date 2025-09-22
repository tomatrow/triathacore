<section>
	<div class="contents">
		<article class="invitation">
			<h3>Your Invitation</h3>
			<h2>Join the TriathaCrew</h2>
			<p>
				We invite you to join us on any one of our monthly rides, runs, and events. Everyone is
				welcome—from seasoned athletes to families just looking to get active together. Check out
				our calendar for local meet-ups and races.
			</p>
			<a class="button button--solid" href="#">View Events Calendar</a>
		</article>

		<article class="partner">
			<h2>Partner with Us</h2>
			<p>
				Are you an organization inspired to build a brighter community for all? We are currently
				looking for supporters and partners to help continue to make our vision a reality. Join us
				in making a sustainable social impact.
			</p>
			<div class="buttons">
				<a class="button button--clear" href="#">Donate Now</a>
				<a class="button button--solid" href="#">Become a Partner</a>
			</div>
		</article>
	</div>
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		padding: 100px 20px;
		background: var(--red);
	}

	.contents {
		display: flex;
		gap: 53px;
		max-width: 845px;
	}

	article.invitation {
		display: flex;
		flex-direction: column;
		gap: 30px;
		color: var(--white);
		position: relative;
		align-items: flex-start;

		h3 {
			color: var(--black);
			position: absolute;
			bottom: 100%;
			margin-bottom: 12px;
		}
	}

	article.partner {
		display: flex;
		flex-direction: column;
		gap: 21px;
		color: var(--white);

		.buttons {
			display: flex;
			gap: 14px;

			.button {
				flex: 1;
			}
		}
	}

	h2 {
		color: #fff;
		font-family: "PP Fuji";
		font-size: 40px;
		font-style: normal;
		font-weight: 700;
		line-height: 88%; /* 35.2px */
		letter-spacing: -0.2px;
	}

	p {
		color: #fff;
		font-feature-settings:
			"liga" off,
			"clig" off;
		font-family: "Sofia Pro";
		font-size: 18.136px;
		font-style: normal;
		font-weight: 500;
		line-height: 160%; /* 29.017px */
	}
</style>
