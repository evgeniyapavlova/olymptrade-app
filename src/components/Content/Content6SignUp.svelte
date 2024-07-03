<script>
	import { base } from '$app/paths';
</script>

<section>
	<h2>Start Trading with Olymp Trade</h2>
	<div class="text">Firstly, you'll need to register an account to unlock full functionality.</div>
	<div class="sign-up-buttons">
		<a href="{base}/" class="button">Email sign-up</a>
		<a href="{base}/" class="button">Social media sign-up</a>
		<a href="{base}/" class="button">Mobile sign-up</a>
	</div>
</section>

<style>
	section {
		text-align: center;
		padding-bottom: 60px;
		border-bottom: 1px solid rgba(0, 0, 0, 0.2);
	}
	.sign-up-buttons {
		display: flex;
		justify-content: center;
		gap: 60px;
	}
	h2 {
		margin-bottom: 20px;
	}
	.text {
		margin-bottom: 40px;
	}

	@media screen and (max-width: 960px) {
		.sign-up-buttons {
			flex-direction: column;
			align-items: center;
			gap: 20px;
		}
	}
</style>
