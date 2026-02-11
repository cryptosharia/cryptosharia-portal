<script lang="ts">
	let { title, subtitle } = $props();
</script>

<header class="flex flex-col items-center mb-10">
	<div
		class="shadow-orange-500/20 mb-4 flex h-14 w-14 items-center justify-center rounded-2xl bg-gradient-to-br from-orange-400 to-orange-600 shadow-lg"
	>
		<svg class="h-8 w-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2.5"
				d="M13 10V3L4 14h7v7l9-11h-7z"
			></path>
		</svg>
	</div>
	<h2 class="text-sm font-bold uppercase tracking-[0.3em] text-brand-orange">CryptoSharia</h2>
</header>

<section class="space-y-6 text-center">
	<h1 class="text-gradient text-4xl font-extrabold leading-[1.15] md:text-5xl">
		{@html title}
	</h1>
	<p class="mx-auto max-w-md text-lg leading-relaxed text-slate-400">
		{subtitle}
	</p>
</section>
