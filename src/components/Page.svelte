<script>
	import Header from './Header/Header.svelte';
	import Intro from './Intro/Intro.svelte';
	export let content;
</script>

<div class="intro">
	<Header content={content.header} />
	<Intro content={content.intro} />
</div>

<style>
	.intro {
		background-image: linear-gradient(300deg, #334061 0, #131720 100%);
	}
</style>
