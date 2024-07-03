<script>
	import { base } from '$app/paths';
	import generateRandomColor from '$lib/utils/randomColor';
	import { Splide, SplideSlide } from '@splidejs/svelte-splide';
	import '@splidejs/svelte-splide/css';

	const options = {
		drag: true,
		type: 'loop',
		focus: 'center',
		gap: '20px',
		arrows: false,
		pagination: false,
		speed: 800,
		perPage: 3,
		perMove: 1,
		autoplay: true,
		breakpoints: {
			1024: {
				focus: 0,
				autoWidth: true
			}
		}
	};

	const items = [
		{
			quote: 'Excellent mobile trading app',
			author: 'Rajesh, Mumbai',
			text: 'Rajesh uses the Android app and finds it reliable with an excellent interface. He likes the instant notifications for market movements which help him make decisions.'
		},
		{
			quote: 'Smooth experience on my iPhone',
			author: 'Priya, Delhi',
			text: 'Priya trades stocks and commodities on her iPhone. She appreciates the intuitive gestures and deep analysis features providing insights for her trading.'
		},
		{
			quote: 'Powerful Windows software for analysis',
			author: 'Saurav, Bangalore',
			text: 'Saurav uses the Olymp Trade Windows software on his laptop for technical analysis. He finds it very fast with a wide range of indicators helping his intraday trading.'
		},
		{
			quote: 'Mac app meets all my trading needs',
			author: 'Leela, Hyderabad',
			text: 'For Leela, the Mac trading application offers everything she needs in one place. She likes the multiple workspaces allowing her to track different assets and execute her strategies.'
		},
		{
			quote: 'Expert advisor helps my crypto trading',
			author: 'Raj, Chennai',
			text: 'Raj works full time so uses an expert advisor integrated into the Desktop app to automate his Bitcoin trades. This functionality is unavailable on the browser version.'
		},
		{
			quote: 'Smooth cross-device usage',
			author: 'Amit, Kolkata',
			text: 'Amit seamlessly uses a combination of the Android app when on the go and the Desktop platform for more detailed analysis in the evenings. His account, transactions, data sync across both platforms.'
		}
	];
</script>

<section class="reviews">
	<h2>Olymp Trade Users Share Their App Experiences</h2>
	<div class="text">
		See what real Olymp Trade traders from India think about using the company's mobile and desktop
		applications:
	</div>

	<div class="slider-wrap">
		<Splide aria-label="Users reviews" {options}>
			{#each items as item}
				<SplideSlide>
					<div class="review">
						<div class="review-quote">
							<img src="{base}/images/svg/quote_left.svg" alt="Quote" />
							<i>{item.quote}</i>
						</div>
						<div class="review-text">
							{item.text}
						</div>
						<div class="review-author">
							<div class="review-avatar" style="background-color: #{generateRandomColor()}">
								{item.author[0]}
							</div>
							<div class="review-name">
								{item.author}
							</div>
						</div>
					</div>
				</SplideSlide>
			{/each}
		</Splide>
	</div>
</section>

<style>
	h2 {
		margin-bottom: 20px;
	}
	.review {
		display: flex;
		flex-direction: column;
		cursor: pointer;
	}

	:global(.reviews .splide__list) {
		align-items: stretch;
	}
	.review {
		padding: 24px;
		background-color: white;
		border: 1px solid rgba(0, 0, 0, 0.1);
		border-radius: 10px;
		margin-top: 10px;
		margin-bottom: 10px;
		height: calc(100% - 20px);
		background-color: rgba(0, 0, 0, 0.02);
	}

	section {
		padding-bottom: 60px;
	}

	.review-quote {
		position: relative;
		padding: 34px 0 20px 0;
		font-size: 20px;
		line-height: 1.3;
	}

	.review-quote img {
		position: absolute;
		left: 0;
		top: -4px;
	}

	.review-author {
		display: flex;
		align-items: flex-end;
		justify-content: flex-start;
		gap: 12px;
		margin-top: 20px;
		flex-grow: 1;
	}

	.review-avatar {
		color: white;
		font-weight: 700;
		width: 40px;
		height: 40px;
		border-radius: 40px;
		display: flex;
		align-items: center;
		justify-content: center;
		line-height: 1;
	}

	.review-text {
		color: rgba(0, 0, 0, 0.7);
		font-size: 16px;
	}

	.text {
		text-align: center;
		margin-bottom: 40px;
	}

	@media screen and (max-width: 1024px) {
		.review {
			width: 320px;
			padding: 20px;
		}
		.review-author {
			margin-top: 10px;
		}
	}

	@media screen and (max-width: 768px) {
		.review-quote {
			font-size: 18px;
			padding-bottom: 10px;
		}
		.review-text {
			font-size: 14px;
		}
		.review {
			width: 250px;
		}
		section {
			padding-bottom: 20px;
		}
	}

	@media screen and (max-width: 600px) {
		.slider-wrap {
			margin-right: -24px;
			width: calc(100vw - 24px);
		}
	}
</style>
