<script lang="ts">
	let { href, title, description, icon = '', type = 'default' } = $props();
</script>

<a {href} target="_blank" rel="noopener noreferrer" class="group block">
	<div
		class="glass-card relative flex items-center gap-5 overflow-hidden rounded-[2.5rem] p-6
        {type === 'primary' ? 'orange-glow' : ''}
        {type === 'catalog'
			? 'flex-col space-y-4 rounded-[2.5rem] border border-primary/20 bg-primary/10 p-8 text-center transition-all hover:bg-primary/20'
			: ''}"
	>
		{#if type === 'catalog'}
			<div
				class="inline-flex items-center gap-2 rounded-full border border-primary/30 bg-primary/10 px-4 py-1.5 text-[10px] font-black tracking-[0.2em] text-primary uppercase"
			>
				<span class="relative flex h-2 w-2">
					<span
						class="absolute inline-flex h-full w-full animate-ping rounded-full bg-primary opacity-75"
					></span>
					<span class="relative inline-flex h-2 w-2 rounded-full bg-primary"></span>
				</span>
				Premium
			</div>

			<div class="space-y-3">
				<h4 class="text-3xl font-black tracking-tight text-foreground">{title}</h4>
				<p class="mx-auto max-w-sm text-sm leading-relaxed text-faded">
					{description}
				</p>
			</div>

			<div
				class="flex items-center justify-center gap-3 rounded-2xl bg-primary px-8 py-4 text-base font-black text-on-primary shadow-xl shadow-primary/30 transition-all duration-300 group-hover:scale-[1.02] group-hover:brightness-110 active:scale-95"
			>
				<span>Lihat Katalog</span>
				<svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2.5"
						d="M14 5l7 7m0 0l-7 7m7-7H3"
					></path>
				</svg>
			</div>

			<p class="text-[10px] font-medium tracking-widest text-faded uppercase opacity-60">
				Dikelola langsung oleh Tim CryptoSharia
			</p>
		{:else}
			{#if type === 'primary'}
				<div
					class="pointer-events-none absolute top-0 right-0 h-full w-32 bg-primary/5 blur-3xl"
				></div>
			{/if}
			<div
				class="flex h-14 w-14 shrink-0 items-center justify-center rounded-2xl text-2xl transition-transform group-hover:scale-110
                {type === 'wa' ? 'bg-green-500/10' : ''}
                {type === 'discord' ? 'bg-indigo-500/10' : ''}
                {type === 'admin' ? 'bg-surface' : ''}"
			>
				{icon}
			</div>
			<div class="flex-1 text-left">
				<h3 class="text-lg font-bold text-foreground">{title}</h3>
				<p class="text-xs text-faded">{description}</p>
			</div>
			<div class="text-line transition-colors group-hover:text-primary">
				<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M14 5l7 7m0 0l-7 7m7-7H3"
					></path>
				</svg>
			</div>
		{/if}
	</div>
</a>

<style>
	/* Explicitly defining types for conditional classes if needed, but handled by Tailwind 4 */
</style>
