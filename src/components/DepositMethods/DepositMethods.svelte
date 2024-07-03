<script>
	import { base } from '$app/paths';
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
		perPage: 5,
		perMove: 5,
		autoplay: true,
		breakpoints: {
			1024: {
				focus: 0,
				autoWidth: true
			}
		}
	};

	const methods = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
</script>

<div>
	<Splide aria-label="Deposite methods" {options}>
		{#each methods as method}
			<SplideSlide>
				<img src="{base}/images/svg/DM{method}.svg" alt="Deposit method" />
			</SplideSlide>
		{/each}
	</Splide>
</div>

<style>
	div {
		margin-top: 60px;
		max-width: 960px;
		cursor: pointer;
		margin-bottom: 70px;
		margin-left: auto;
		margin-right: auto;
	}
	img {
		height: 80px;
	}

	@media screen and (max-width: 768px) {
		div {
			margin-top: 30px;
			margin-bottom: 40px;
		}
		img {
			height: 60px;
		}
	}
</style>
