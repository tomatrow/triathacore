<script lang="ts">
	import logo from '$lib/assets/logo.svg';
</script>

<section>
	<header>
		<a href="/">
			<img src={logo} alt="Triathacore Logo" />
		</a>
		<div class="links">
			<a class="link" target="_blank" href="https://luma.com/triathacore">Events</a>
			<a class="link" target="_blank" href="mailto:triathacore@gmail.com">Contact</a>
			<a
				class="button"
				href="https://www.gofundme.com/f/support-team-triathacores-inclusive-racing?attribution_id=sl:5776503b-941d-4946-ae04-9cb32e2fc8d8&lang=en_US&ts=1758334116&utm_campaign=fp_sharesheet&utm_content=amp13_c-amp17_control&utm_medium=customer&utm_source=copy_link"
				>Donate Now</a
			>
		</div>
	</header>
</section>

<style>
	section {
		background: var(--red);
		display: flex;
		justify-content: center;
		padding: 20px;
	}

	header {
		display: flex;
		max-width: 924px;
		justify-content: space-between;
		align-items: center;
		width: 100%;
	}

	.links {
		display: flex;
		align-items: center;
		gap: 24px;
	}
</style>
