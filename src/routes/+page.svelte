<script>
	import meta_img from '$lib/images/meta_img_main.jpg';
	import content from '../translations/en';
	import Page from '$comps/Page.svelte';

	const title = 'Download and Install Olymp Trade Platform Apps for PC and Mobile in 2024';
	const desc =
		"Looking to download Olymp Trade's trading apps? Get step-by-step instructions to install Olymp Trade for Android, iOS, Windows, Mac, and APK in India.";
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={desc} />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={desc} />
	<meta property="og:image" content={meta_img} />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={desc} />
	<meta name="twitter:image" content={meta_img} />
</svelte:head>

<Page {content} />
