<script>
	import { base } from '$app/paths';
	import links from '$lib/utils/links';
	import LazyImage from '$comps/LazyImage/LazyImage.svelte';
	import Rating from './Rating.svelte';
	export let content;
</script>

<section>
	<div class="intro-left">
		<h1>{@html content.h1}</h1>
		<a href={links.start} class="button"> {content.start}</a>
		<Rating reviewsText={content.reviews} />
	</div>
	<div class="intro-img-wrap">
		<div class="intro-img-wrap-inner">
			<LazyImage className="intro-img" alt="Intro screens" src="{base}/images/devices.webp" />
		</div>
	</div>
</section>

<style>
	section {
		display: flex;
		align-items: center;
		justify-content: space-between;
		color: white;
		padding-top: 40px;
		padding-bottom: 120px;
	}
	h1 {
		font-size: 58px;
		font-weight: 600;
		line-height: 1;
		margin-bottom: 32px;
	}
	.intro-img-wrap,
	.intro-left {
		width: 50%;
	}
	.intro-img-wrap-inner {
		width: 120%;
		margin-right: -20%;
		padding-bottom: 74%;
		position: relative;
	}

	:global(.intro-img) {
		width: 100%;
		position: absolute;
		display: block;
	}
	@media screen and (max-width: 1630px) {
		.intro-img-wrap-inner {
			width: 100%;

			padding-bottom: 61%;
			position: relative;
		}

		h1 {
			font-size: 50px;
		}
	}

	@media screen and (max-width: 1024px) {
		h1 {
			font-size: 40px;
			line-height: 1.2;
		}

		section {
			display: block;
			text-align: center;
		}
		.intro-img-wrap,
		.intro-left {
			width: 100%;
		}

		.intro-left {
			margin-bottom: 60px;
		}
	}

	@media screen and (max-width: 768px) {
		h1 {
			font-size: 30px;
		}

		section {
			padding-bottom: 80px;
		}
	}

	@media screen and (max-width: 600px) {
		section {
			padding-bottom: 60px;
		}
	}
</style>
