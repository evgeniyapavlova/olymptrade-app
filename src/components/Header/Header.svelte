<script>
	import links from '$lib/utils/links';
	import logo from '$lib/images/logo.svg';
	export let content;
</script>

<header>
	<section>
		<img class="header-logo" src={logo} alt="Olymp Trade logotype" />
		<a class="button" href={links.signUp} target="_blank">
			{content.signUp}
		</a>
	</section>
</header>

<style>
	section {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding-top: 40px;
		padding-bottom: 40px;
	}
	.header-logo {
		width: 270px;
	}

	@media screen and (max-width: 1280px) {
		.header-logo {
			width: 200px;
		}

		section {
			padding-top: 24px;
			padding-bottom: 24px;
		}
	}

	@media screen and (max-width: 768px) {
		.button {
			display: none;
		}
	}
</style>
