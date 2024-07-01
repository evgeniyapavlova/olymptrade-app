<script>
	import Accordion from '$comps/Accordion/Accordion.svelte';
	const items = [
		{
			question: 'Is the desktop app secure to install?',
			text: "Yup! Before release, Olymp Trade checks all their desktop apps thoroughly for viruses/malware, so you're good to download."
		},
		{
			question: 'What kind of advanced analysis is available?',
			text: 'Great question! Their desktop application comes loaded with tons of handy indicators — and it responds way faster than the web version. So, technical analysis will be a breeze.'
		},
		{
			question: 'How fast should my internet connection be?',
			text: "For the best experience, you'll want your internet speed to be at least 5 Mbps. Note that the platform doesn't work offline."
		},
		{
			question: 'Can I download an official Olymp Trade app?',
			text: 'Absolutely! They offer free mobile applications for Android and iOS in the app stores. There are also desktop applications for Windows and Mac that you can download from their website.'
		},
		{
			question: "What's the process for installing the software?",
			text: 'Getting the mobile apps just takes searching for "Olymp Trade" in the Google Play or App Store. For the PC/Mac applications, go to olymptrade.com/download where you\'ll find the installers.'
		},
		{
			question: 'How does it work for laptop installation?',
			text: 'On Windows laptops, go to Olymp Trade’s desktop apps page, get the EXE file, double-click to launch the installer, and follow the prompts. The flow would be the same for MacBooks, with the only exception that you’ll be downloading the DMG file.'
		},
		{
			question: 'Can I find it in the App Store?',
			text: 'Yep! The official iOS application by Olymp Trade Inc. can be downloaded from the App Store for free — just look for "Olymp Trade". The app works on iPhones, iPads, and iPods.'
		},
		{
			question: 'Can I trade across multiple devices?',
			text: 'Absolutely! You can use your Olymp Trade account across all your devices (smartphone, tablet, or laptop).'
		},
		{
			question: 'Is a practice account offered?',
			text: 'Yes. You get access to a free demo account loaded with $10,000 in virtual funds to sharpen your skills before trading on the real market.'
		}
	];
</script>

<section>
	<h2>Olymp Trade Desktop Apps FAQ</h2>
	{#each items as item}
		<Accordion {item} />
	{/each}
</section>

<style>
	section {
		padding-top: 40px;
		padding-bottom: 60px;
	}
</style>
