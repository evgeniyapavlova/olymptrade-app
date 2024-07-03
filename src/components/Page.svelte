<script>
	import Header from './Header/Header.svelte';
	import Intro from './Intro/Intro.svelte';
	import Content from './Content/Content.svelte';
	import Content2 from './Content/Content2.svelte';
	import Content3IOSAndroid from './Content/Content3IOSAndroid.svelte';
	import Screenshots from './Content/Screenshots.svelte';
	import Content4DesktopApps from './Content/Content4DesktopApps.svelte';
	import Content5HowToInstall from './Content/Content5HowToInstall.svelte';
	import Content6SignUp from './Content/Content6SignUp.svelte';
	import Content6Reviews from './Content/Content6_1Reviews.svelte';
	import Content7WrappingUp from './Content/Content7WrappingUp.svelte';
	import Content8Faq from './Content/Content8FAQ.svelte';
	import Footer from './Footer/Footer.svelte';
	export let content;
</script>

<div class="intro">
	<Header content={content.header} />
	<Intro content={content.intro} />
</div>

<Content />

<Screenshots />

<Content2 />

<Content3IOSAndroid />

<Content4DesktopApps />
<Content5HowToInstall />

<Content6SignUp />
<Content6Reviews />
<Content7WrappingUp />

<Content8Faq />

<Footer />

<style>
	.intro {
		background-image: linear-gradient(300deg, #334061 0, #131720 100%);
	}
</style>
