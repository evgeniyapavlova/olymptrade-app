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
				<li>Trade on the go wherever you are</li>
				<li>The intuitive interface makes navigation super smooth</li>
				<li>Real-time price alerts keep you informed</li>
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
				<li>Faster performance</li>
				<li>Extra tools like Expert Advisors</li>
				<li>Multi-screen support</li>
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
				<li>Convenient access anywhere</li>
				<li>No installation needed</li>
				<li>Cross-device login sync</li>
			</ul>
			<a href={links.web} class="button" target="_blank">Go to web</a>
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
		<li>Learn risk-free</li>
		<li>Test strategies</li>
		<li>Understand analyses</li>
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
		justify-content: center;
		gap: 20px;
	}
	:global(.app-btn) {
		width: 180px;
	}

	:global(.text-img) {
		max-width: 100%;
	}
</style>
