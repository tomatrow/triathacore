<script lang="ts">
	import { resolve } from "$app/paths"
	import footerData from "$lib/cms_data/footer.json"
	import logo from "$lib/assets/logo.svg"
</script>

<footer>
	<nav>
		<a href={resolve("/")}>
			<img src={logo} alt="Triathacore Logo" />
		</a>

		<div class="nav-links">
			{#each footerData.navItems as navItem, index (index)}
				<a class="link" target="_blank" href={navItem.link}>{navItem.label}</a>
			{/each}
		</div>
	</nav>

	<p>
		© 2025, Triathacore
		<br />
		Site By <a target="_blank" href="https://redbike.agency">Red Bike Agency</a>
	</p>
</footer>

<style>
	footer {
		color: white;
		background: var(--red);
		padding: 20px;
		display: flex;
		flex-direction: column;
		align-items: center;

		nav {
			display: flex;
			max-width: 925px;
			width: 100%;
			flex-direction: column;
			align-items: center;
			gap: 20px;

			@media (min-width: 500px) {
				flex-direction: row;
				justify-content: space-around;
			}
		}

		.nav-links {
			display: flex;
			gap: 28px;
		}

		p {
			color: #fff;
			text-align: center;
			font-family: "Sofia Pro";
			font-size: 16px;
			font-style: normal;
			font-weight: 500;
			line-height: 145%; /* 23.2px */
			letter-spacing: -0.08px;
			margin-top: 45px;
		}

		a {
			color: white;
		}
	}
</style>
