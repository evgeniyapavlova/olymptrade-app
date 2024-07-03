<script>
	import { base } from '$app/paths';
	import links from '$lib/utils/links';
	import LazyImage from '$comps/LazyImage/LazyImage.svelte';
	import DesktopApps from './DesktopApps.svelte';
</script>

<section>
	<div class="text">
		Let's check out how you can access Olymp Trade's slick trading platform on both your desktop and
		mobile devices. Traders can use the same powerful platform to easily manage their accounts on
		Windows, Mac, Android, iOS, and web browsers.
	</div>

	<!-- <LazyImage
		src="{base}/images/man.webp"
		alt="Indian man using multiple devices - phone, tablet and laptop - to access Olymp Trade platform"
		className="img1"
	/> -->

	<h2>See Olymp Trade's Apps Tailored to Traders</h2>
	<div class="flex-text flex-text-right">
		<div>
			<div class="text">
				First up, Olymp Trade has mobile apps made for Android and iOS phones and tablets. Here's
				what you get:
			</div>
			<ul>
				<li><span>Trade on the go wherever you are</span></li>
				<li><span>The intuitive interface makes navigation super smooth</span></li>
				<li><span>Real-time price alerts keep you informed</span></li>
			</ul>
			<div class="app-store-btns">
				<a href={links.appStore} target="_blank">
					<LazyImage
						src="{base}/images/app-store-large.webp"
						alt="Download on the AppStore"
						className="app-btn"
					/>
				</a>
				<a href={links.appStore} target="_blank">
					<LazyImage
						src="{base}/images/google-play-large.webp"
						alt="Get it on Google Play"
						className="app-btn"
					/>
				</a>
			</div>
		</div>
		<div>
			<LazyImage
				src="{base}/images/img1.webp"
				alt="Mobile applications for Android and iOS phones and tablets"
				className="img1 text-img"
			/>
		</div>
	</div>
	<div class="flex-text flex-text-left">
		<div>
			<LazyImage src="{base}/images/img2.webp" alt="Desktop apps" className="img2 text-img" />
		</div>
		<div>
			<div class="text">
				Additionally, they offer desktop apps specially designed for Windows and Mac. These give
				you:
			</div>

			<ul>
				<li><span>Faster performance</span></li>
				<li><span>Extra tools like Expert Advisors</span></li>
				<li><span>Multi-screen support</span></li>
			</ul>

			<DesktopApps />
		</div>
	</div>

	<div class="flex-text flex-text-right">
		<div>
			<div class="text">
				There's also Olymp Trade's web-based platform that you can access on any modern browser. The
				perks here include:
			</div>

			<ul>
				<li><span>Convenient access anywhere</span></li>
				<li><span>No installation needed</span></li>
				<li><span>Cross-device login sync</span></li>
			</ul>
			<div class="text">
				<a href={links.web} class="button" target="_blank">Go to web</a>
			</div>
		</div>
		<div>
			<LazyImage
				src="{base}/images/img3.webp"
				alt="Indian man using multiple devices - phone, tablet and laptop - to access Olymp Trade platform"
				className="img3 text-img"
			/>
		</div>
	</div>

	<div class="text">
		And check this out — OlympTrade has free $10,000 practice accounts! These let you:
	</div>

	<ul>
		<li><span>Learn risk-free</span></li>
		<li><span>Test strategies</span></li>
		<li><span>Understand analyses</span></li>
	</ul>

	<div class="text">
		Finally, signing up with Olymp Trade is super easy — you can do it via email, social media, or
		mobile.
	</div>
</section>

<style>
	section {
		padding-top: 100px;
		padding-bottom: 60px;
	}

	.app-store-btns {
		display: flex;
		align-items: center;
		justify-content: flex-start;
		gap: 20px;
		margin-left: -15px;
	}
	:global(.app-btn) {
		width: 180px;
	}

	:global(.text-img) {
		max-width: 100%;
	}

	@media screen and (max-width: 768px) {
		section {
			padding-top: 60px;
		}
		.flex-text-left {
			display: flex;
			flex-direction: column-reverse;
		}
		a.button {
			margin-left: auto;
			margin-right: auto;
			display: inline-block;
		}

		.app-store-btns {
			gap: 0;
			margin-left: 0;
			justify-content: center;
		}
	}

	@media screen and (max-width: 400px) {
		.app-store-btns {
			display: block;
			text-align: center;
		}
	}
</style>
