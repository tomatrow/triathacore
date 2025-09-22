<script lang="ts">
	import { Menu, X } from "@lucide/svelte"
	import logo from "$lib/assets/logo.svg"

	let isMenuOpen = $state(false)
</script>

<section>
	<header>
		<a href="/">
			<img src={logo} alt="Triathacore Logo" />
		</a>

		<button class="mobile-menu-button" onclick={() => (isMenuOpen = true)}>
			<Menu />
		</button>

		{#if isMenuOpen}
			<div class="mobile-links">
				<a class="mobile-logo" href="/">
					<img src={logo} alt="Triathacore Logo" />
				</a>
				<a class="link" target="_blank" href="https://luma.com/triathacore">Events</a>
				<a class="link" target="_blank" href="mailto:triathacore@gmail.com">Contact</a>
				<a
					class="button button--solid"
					href="https://www.gofundme.com/f/support-team-triathacores-inclusive-racing?attribution_id=sl:5776503b-941d-4946-ae04-9cb32e2fc8d8&lang=en_US&ts=1758334116&utm_campaign=fp_sharesheet&utm_content=amp13_c-amp17_control&utm_medium=customer&utm_source=copy_link"
					>Donate Now</a
				>
				<button class="mobile-close-button" onclick={() => (isMenuOpen = false)}>
					<X />
				</button>
			</div>
		{/if}

		<div class="desktop-links">
			<a class="link" target="_blank" href="https://luma.com/triathacore">Events</a>
			<a class="link" target="_blank" href="mailto:triathacore@gmail.com">Contact</a>
			<a
				class="button button--solid"
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

	section {
		.mobile-menu-button {
			color: white;

			@media (min-width: 700px) {
				display: none;
			}
		}

		.mobile-close-button {
			color: white;
			position: absolute;
			top: 2rem;
			right: 2rem;
		}

		.mobile-links {
			display: flex;
			flex-direction: column;
			gap: 32px;
			padding: 20px;
			align-items: flex-start;
			justify-content: center;
			position: absolute;
			inset: 0;
			background: var(--red);
			z-index: 1000;

			.mobile-logo {
				position: absolute;
				top: 2rem;
				left: 1rem;
			}

			@media (min-width: 700px) {
				display: none;
			}
		}
	}

	.desktop-links {
		display: none;
		align-items: center;
		gap: 24px;

		@media (min-width: 700px) {
			display: flex;
		}
	}
</style>
