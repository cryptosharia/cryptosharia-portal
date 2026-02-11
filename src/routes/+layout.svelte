<script lang="ts">
	import './layout.css';
	import ThemeSwitcher from '$lib/components/ThemeSwitcher.svelte';
	import { SvelteTheme } from 'svelte-themes';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/favicon.ico" />
	<title>CryptoSharia Portal</title>
</svelte:head>

<SvelteTheme enableSystem defaultTheme="system" attribute="class" enableColorScheme>
	{@render children()}
	<ThemeSwitcher />
</SvelteTheme>
