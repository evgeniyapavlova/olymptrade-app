<script>
	import links from '$lib/utils/links';
	import logo from '$lib/images/logo.svg';
	export let content;
</script>

<header>
	<section>
		<img src={logo} alt="" width="270" />
		<a class="button" href={links.signUp}>
			{content.signUp}
		</a>
	</section>
</header>

<style>
	section {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 40px 0;
	}
</style>
