<script lang="ts">
	import invitationSection from "$lib/cms_data/invitation-section.json"
</script>

<section>
	<div class="contents">
		<article class="invitation">
			<h3>{invitationSection.eventsSubtitle}</h3>
			<h2>{invitationSection.eventsTitle}</h2>
			<p>{invitationSection.eventsText}</p>
			<a class="button button--solid" target="_blank" href={invitationSection.eventsButtonLink}
				>{invitationSection.eventsButtonText}</a
			>
		</article>

		<article class="partner">
			<h2>{invitationSection.partnerTitle}</h2>
			<p>{invitationSection.partnerText}</p>
			<div class="buttons">
				<a
					class="button button--clear"
					target="_blank"
					href={invitationSection.leftPartnerButtonLink}
					>{invitationSection.leftPartnerButtonText}</a
				>
				<a
					class="button button--solid"
					target="_blank"
					href={invitationSection.rightPartnerButtonLink}
					>{invitationSection.rightPartnerButtonText}</a
				>
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
		flex-direction: column;

		@media (min-width: 845px) {
			max-width: 845px;
			flex-direction: row;
		}
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
			flex-wrap: wrap;

			.button {
				flex: 1;
				min-width: 10rem;
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
