<script lang="ts">
	import logo from '$lib/assets/logo.png';
	let { title, subtitle } = $props();
</script>

<header class="mb-10 flex flex-col items-center">
	<div class="relative mb-6">
		<div
			class="absolute -inset-4 animate-pulse rounded-full bg-primary/20 blur-2xl transition-opacity"
		></div>
		<img src={logo} alt="CryptoSharia Logo" class="relative h-20 w-auto" />
	</div>
	<h2 class="text-sm font-black tracking-[0.4em] text-primary uppercase">CryptoSharia</h2>
</header>

<section class="space-y-6 text-center">
	<h1 class="text-gradient fl-text-2xl/4xl leading-[1.15] font-extrabold">
		{@html title}
	</h1>
	<p class="mx-auto max-w-md fl-text-base/lg leading-relaxed text-faded">
		{subtitle}
	</p>
</section>
