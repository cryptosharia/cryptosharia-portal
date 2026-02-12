<script lang="ts">
	import './layout.css';
	import ThemeSwitcher from '$lib/components/ThemeSwitcher.svelte';
	import { SvelteTheme } from 'svelte-themes';

	let { children } = $props();

	const siteTitle = 'CryptoSharia Portal';
	const siteDescription =
		'Wadah belajar dan komunitas Muslim untuk menavigasi dunia Web3 serta crypto dengan prinsip syariah.';
	const siteUrl = 'https://portal.cryptosharia.id';
	const ogImage = `${siteUrl}/og-image.png`;
</script>

<svelte:head>
	<link rel="icon" href="/favicon.ico" />
	<title>{siteTitle}</title>
	<meta name="description" content={siteDescription} />
	<meta name="keywords" content="crypto sharia, kripto syariah, belajar crypto, komunitas web3" />

	<!-- Open Graph / Facebook / WhatsApp -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="{siteUrl}/" />
	<meta property="og:title" content={siteTitle} />
	<meta property="og:description" content={siteDescription} />
	<meta property="og:image" content={ogImage} />

	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="{siteUrl}/" />
	<meta property="twitter:title" content={siteTitle} />
	<meta property="twitter:description" content={siteDescription} />
	<meta property="twitter:image" content={ogImage} />
</svelte:head>

<SvelteTheme enableSystem defaultTheme="system" attribute="class" enableColorScheme>
	{@render children()}
	<ThemeSwitcher />
</SvelteTheme>
