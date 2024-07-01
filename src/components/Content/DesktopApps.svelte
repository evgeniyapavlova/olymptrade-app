<script>
	import links from '$lib/utils/links';

	import MacOs from './svg/MacOS.svelte';
	import Windows from './svg/Windows.svelte';
	import WebApp from './svg/WebApp.svelte';

	const desktopApps = [
		{
			label: 'Windows x32',
			icon: Windows,
			link: links.windows32
		},
		{ label: 'MacOS', icon: MacOs, link: links.macOS },
		{
			label: 'Windows x64',
			icon: Windows,
			link: links.windows64
		},

		{ label: 'WebApp', icon: WebApp, link: links.webApp }
	];
</script>

<div class="desktop-apps-list">
	{#each desktopApps as desktopApp}
		<a href={desktopApp.link} alt="{desktopApp.label} download" class="text" target="_blank">
			<svelte:component this={desktopApp.icon} />
			{desktopApp.label}
		</a>
	{/each}
</div>

<style>
	.desktop-apps-list {
		display: flex;
		flex-wrap: wrap;
		max-width: 360px;
		margin-top: 40px;
	}

	.desktop-apps-list > a {
		width: 50%;
		display: flex;
		align-items: center;
		gap: 10px;
		transition: 0.2s color ease-out;
	}
	:global(.desktop-apps-list > a > svg) {
		width: 20px;
		fill: var(--btn-blue);
		transition: 0.2s fill ease-out;
	}
	:global(.desktop-apps-list > a:hover > svg) {
		fill: var(--main-green);
	}
	.desktop-apps-list > a:hover {
		color: var(--main-green);
	}
</style>
