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
		autoplay: true
	};

	const methods = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
</script>

<section>
	<Splide aria-label="Deposite methods" {options}>
		{#each methods as method}
			<SplideSlide>
				<img src="{base}/images/svg/DM{method}.svg" alt="Deposit method" />
			</SplideSlide>
		{/each}
	</Splide>
</section>

<style>
	section {
		margin-top: 60px;
		max-width: 960px;
		cursor: pointer;
		margin-bottom: 70px;
	}
	img {
		height: 80px;
	}
</style>
