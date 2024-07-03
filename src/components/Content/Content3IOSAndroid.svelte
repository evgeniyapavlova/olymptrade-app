<script>
	import { fade } from 'svelte/transition';
	import { base } from '$app/paths';
	import links from '$lib/utils/links';
	import LazyImage from '$comps/LazyImage/LazyImage.svelte';
	import SwitchContent from '$comps/SwitchContent/SwitchContent.svelte';

	let isFirstActive = true;
</script>

<div class="wrap android-ios">
	<section>
		<h2>Olymp Trade Mobile:<br />for Android and iOS Users</h2>
		<div class="text" style="text-align: center;">
			Olymp Trade offers apps for both Android and iOS devices to enable convenient mobile trading.
		</div>

		<SwitchContent buttonLabels={{ left: 'iOS', right: 'Android' }} bind:isFirstActive />

		<div class="flex-text flex-text-right">
			{#if isFirstActive}
				<div in:fade={{ duration: 500 }}>
					<h3>Get the iOS App on Your iPhone & iPad</h3>
					<div class="text">Olymp Trade's iOS app features:</div>

					<ul>
						<li><span>Real-time pricing/news</span></li>
						<li><span>Intuitive navigation</span></li>
						<li><span>In-depth charts and analysis</span></li>
						<li><span>Robust account privacy</span></li>
					</ul>

					<div class="text">Here's how to install the app on your iPhone:</div>

					<ul>
						<li><span>Visit Olymp Trade's website from your iPhone</span></li>
						<li><span>Click 'Get' to start the installation</span></li>
						<li><span>Find the new Olymp Trade icon and open the app</span></li>
						<li>
							<span
								>Sign up if you’re new to Olymp Trade; otherwise, login with your email and password</span
							>
						</li>
					</ul>

					<div class="text">
						You can also get the app directly from the App Store on devices running the latest iOS.
					</div>
					<div class="text">
						<a href={links.appStore} target="_blank">
							<img
								src="{base}/images/app-store-large.webp"
								alt="Download on the AppStore"
								class="app-btn-1"
							/>
						</a>
					</div>

					<div class="text">
						Now for compatibility details — the iOS app flawlessly supports all models of iPhone,
						iPad, and iPod Touch devices running the most recent iOS versions.
					</div>

					<div class="text">
						In terms of user reviews, the app boasts a stellar 4.7 average rating from 3,000+
						reviews, which proves a high level of user satisfaction.
					</div>
				</div>
			{:else}
				<div in:fade={{ duration: 500 }}>
					<h3>Get the Android APK for Your Gadgets</h3>
					<div class="text">Here are the steps to easily install the Android APK file:</div>
					<ol>
						<li><span>Download Olymptrade APK on your device</span></li>
						<li><span>Enable installation from unknown sources</span></li>
						<li><span>Install the APK file</span></li>
						<li><span>Launch the Olymp Trade app</span></li>
						<li><span>Register an account to start trading</span></li>
					</ol>
					<div class="text">
						Alternatively, you can install the Android app via the Google Play Store.
					</div>
					<div class="text">
						<a href={links.appStore} target="_blank">
							<img
								src="{base}/images/google-play-large.webp"
								alt="Get it on Google Play"
								class="app-btn-1"
							/>
						</a>
					</div>
					<div class="text">Rest assured Olymp Trade's APK is:</div>
					<ul>
						<li><span>Compatible with Android 5.0+</span></li>
						<li><span>Verified safe for Indian users</span></li>
						<li><span>Virus-free — confirmed by Norton and McAfee</span></li>
					</ul>
				</div>
			{/if}

			<div class="img-wrap">
				<LazyImage
					src="{base}/images/ios_android.webp"
					alt="Trade on the Go Olymp Trade apps for Android and iOS"
					className="img1"
				/>
			</div>
		</div>
	</section>
</div>

<style>
	.img-wrap {
		padding-top: 80px;
	}
	.flex-text-right {
		align-items: flex-start;
	}

	.wrap {
		background-color: var(--dark-bgr);
		color: white;
	}

	h2 {
		color: white;
	}

	:global(.apk-img) {
		width: 220px;
		margin-top: 20px;
	}

	:global(.app-btn-1) {
		width: 220px;
		margin-left: -14px;
	}

	.flex-text-right > div:first-child {
		position: relative;
		z-index: 2;
	}

	@media screen and (max-width: 1150px) {
		.flex-text-right > div:first-child {
			width: 60%;
		}
		.flex-text-right > div:last-child {
			width: 30%;
		}
		.img-wrap {
			position: relative;
			z-index: 1;
		}

		:global(.android-ios .img-wrap img) {
			position: absolute;
			right: -50px;
		}
	}

	@media screen and (max-width: 768px) {
		.img-wrap {
			display: none;
		}

		:global(.app-btn-1) {
			margin-left: auto;
		}
	}
</style>
