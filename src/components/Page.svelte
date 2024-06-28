<script>
	import Header from './Header/Header.svelte';
	export let content;
</script>

<div class="intro">
	<Header content={content.header} />
</div>

<style>
	.intro {
		background-image: linear-gradient(300deg, #334061 0, #131720 100%);
	}
</style>
