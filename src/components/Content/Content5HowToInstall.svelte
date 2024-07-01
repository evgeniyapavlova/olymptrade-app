<script>
	import { fade } from 'svelte/transition';
	import { base } from '$app/paths';
	import SwitchContent from '$comps/SwitchContent/SwitchContent.svelte';
	import links from '$lib/utils/links';

	let isFirstActive = true;
</script>

<div class="container">
	<section>
		<div class="content">
			<h3>How to Install the Desktop Apps</h3>
			<div class="text">
				Here are step-by-step tutorials for installing Olymp Trade on your Windows or Mac:
			</div>
			<SwitchContent bind:isFirstActive buttonLabels={{ left: 'Windows', right: 'MacOS' }} />

			{#if isFirstActive}
				<div in:fade={{ duration: 500 }}>
					<ol style="margin-top: 40px;">
						<li>Download the Olymp Trade PC app</li>
						<li>Run the EXE installer</li>
						<li>Follow the prompts</li>
						<li>Launch the app & login</li>
					</ol>

					<div class="download-buttons">
						<a href={links.windows32}>For Windows x32</a>
						<a href={links.windows64}>For Windows x64</a>
						<a href={links.webApp}>WebApp (PWA)</a>
					</div>
				</div>
			{:else}<div in:fade={{ duration: 500 }}>
					<ol style="margin-top: 40px;">
						<li>Get DMG file</li>
						<li>Open and run the installer</li>
						<li>Drag & drop the app into Applications</li>
						<li>Launch the app to register or log in</li>
					</ol>
					<div class="download-buttons">
						<a href={links.macOS}>For MacOS</a>
						<a href={links.pwa}>WebApp(PWA)</a>
					</div>
				</div>
			{/if}

			<h3>Comparing the Web and Desktop Platforms</h3>
			<div class="text">Let's compare some key aspects of the web and desktop platforms:</div>

			<table class="info">
				<thead
					><tr>
						<th>Aspect</th>
						<th>Web</th>
						<th>Desktop App</th>
					</tr>
				</thead>

				<tbody>
					<tr>
						<td>Accessibility</td>
						<td>Any browser device</td>
						<td>Windows & Mac</td>
					</tr>

					<tr
						><td>Real-time quotes</td>
						<td>Yes</td>
						<td>Yes</td></tr
					>
					<tr
						><td>Speed</td>
						<td>Depends on the browser</td>
						<td>Faster/smoother</td></tr
					>
					<tr
						><td>Compatibility</td>
						<td>Various browsers</td>
						<td>Windows & Mac</td></tr
					>
					<tr
						><td>Cost</td>
						<td>Free</td>
						<td>Free</td></tr
					>
					<tr
						><td>Interface</td>
						<td>User-friendly</td>
						<td>Easy to use</td></tr
					>
				</tbody>
			</table>

			<div class="text">
				In summary, both platforms provide similar features. It comes down to personal preference
				and trading style.
			</div>
		</div>
	</section>

	<div class="img-wrap" style="background-image: url({base}/images/desktop_apps.webp);"></div>
</div>

<style>
	.container {
		position: relative;
		background-color: var(--dark-bgr);
		color: white;
	}
	h3 {
		text-align: left;
		color: white;
	}
	.content {
		width: 50%;
		padding-right: 40px;
		padding-bottom: 40px;
	}
	.img-wrap {
		position: absolute;
		left: 50%;
		top: 0;
		width: 50%;
		height: 100%;
		background-repeat: no-repeat;
		background-size: cover;
	}
	:global(.img-wrap-left img) {
		max-width: 100%;
	}
	.download-buttons {
		display: flex;
		align-items: center;
		justify-content: flex-start;
		gap: 40px;
	}

	.download-buttons a {
		border-bottom: 2px solid var(--btn-blue);
		transition: border 0.2s ease-out;
	}

	.download-buttons a:hover {
		border-bottom: 2px solid transparent;
	}
</style>
