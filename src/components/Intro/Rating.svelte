<script>
	import google_play_logo from '$lib/images/google_play_logo.svg';
	import trustpilot_logo from '$lib/images/trustpilot_logo.svg';
	import mouthshut_logo from '$lib/images/mouthshut_logo.svg';
	import RatingStars from './RatingStars.svelte';
	export let reviewsText;

	const items = [
		{ text: 'Google Play', icon: google_play_logo, rating: '4.8', num: '946k', percent: 80 },
		{ text: 'Trustpilot', icon: trustpilot_logo, rating: '4.4', num: '242', percent: 40 },
		{ text: 'Mouthshut', icon: mouthshut_logo, rating: '4.4', num: '6,551', percent: 40 }
	];
</script>

<div class="intro-items">
	{#each items as item}
		<div class="item">
			<div class="item-name-logo">
				<div class="item-text">{item.text}</div>
				<img class="item-icon" src={item.icon} alt={item.text} />
			</div>
			<div class="item-rating">{item.rating}</div>
			<RatingStars percent={item.percent} />
			<div class="item-caption">
				{item.num}
				{reviewsText}
			</div>
		</div>
	{/each}
</div>

<style>
	.item-rating {
		font-weight: 700;
		font-size: 26px;
		line-height: 1.2;
	}
	.item-text {
		font-weight: 600;
		font-size: 16px;
	}
	.item-icon {
		height: 24px;
		display: block;
	}
	.intro-items {
		display: flex;
		font-weight: 400;
		gap: 40px;
		margin-top: 40px;
	}
	.item-name-logo {
		display: flex;
		align-items: center;
		gap: 6px;
	}
	.item-caption {
		font-weight: 400;
		font-size: 14px;
		line-height: 1;
	}

	@media screen and (max-width: 1024px) {
		.intro-items {
			justify-content: center;
		}
	}
	@media screen and (max-width: 600px) {
		.item-text {
			font-size: 14px;
		}
		.item-name-logo {
			flex-direction: column-reverse;
			margin-bottom: 8px;
		}
		.item-caption {
			font-size: 12px;
		}
		.item-rating {
			line-height: 1;
		}
	}

	@media screen and (max-width: 380px) {
		.intro-items {
			gap: 20px;
		}
	}

	@media screen and (max-width: 340px) {
		.intro-items {
			gap: 10px;
		}
	}
</style>
