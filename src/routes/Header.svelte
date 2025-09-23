<script lang="ts">
	import { Menu, X } from "@lucide/svelte"
	import { resolve } from "$app/paths"
	import Logo from "$lib/assets/Logo.svelte"
	import headerData from "$lib/cms_data/header.json"
	import { fly } from "svelte/transition"
	import { quartOut } from "svelte/easing"

	let isMenuOpen = $state(false)

	$effect(() => {
		if (isMenuOpen) {
			document.body.classList.add("no-scroll")
		} else {
			document.body.classList.remove("no-scroll")
		}
	})
</script>

<section>
	<header>
		<a href={resolve("/")}>
			<Logo />
		</a>

		<button class="mobile-menu-button" onclick={() => (isMenuOpen = true)}>
			<Menu />
		</button>

		{#if isMenuOpen}
			<div class="mobile-links" transition:fly={{ x: -500, easing: quartOut }}>
				<a class="mobile-logo" href={resolve("/")}>
					<Logo />
				</a>

				{#each headerData.navItems as navItem, index (index)}
					{#if navItem.style === "plain"}
						<a class="link" target="_blank" href={navItem.link}>{navItem.label}</a>
					{:else if navItem.style === "button"}
						<a class="button button--solid" href={navItem.link}>{navItem.label}</a>
					{/if}
				{/each}

				<button class="mobile-close-button" onclick={() => (isMenuOpen = false)}>
					<X />
				</button>
			</div>
		{/if}

		<div class="desktop-links">
			{#each headerData.navItems as navItem, index (index)}
				{#if navItem.style === "plain"}
					<a class="link" target="_blank" href={navItem.link}>{navItem.label}</a>
				{:else if navItem.style === "button"}
					<a class="button button--solid" href={navItem.link}>{navItem.label}</a>
				{/if}
			{/each}
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
			position: fixed;
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

	:global {
		.no-scroll {
			overflow: hidden;
		}
	}
</style>
