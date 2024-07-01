<script>
	import { base } from '$app/paths';
</script>

<div style="background-color: #0f1112;">
	<section>
		<div class="img-container" style="background-image: url({base}/images/screenshots.webp)"></div>
	</section>
</div>

<style>
	.img-container {
		padding-bottom: 49%;
		background-size: 100% auto;
		background-repeat: no-repeat;
		width: 100%;
		margin: 60px 0;
	}
	@media screen and (max-width: 600px) {
		.img-container {
			margin: 32px 0;
		}
	}
</style>
