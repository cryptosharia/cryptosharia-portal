<script lang="ts">
	let { href, title, description, icon = '', type = 'default' } = $props();
</script>

<a {href} class="group block">
	<div
		class="glass-card relative flex items-center gap-5 overflow-hidden rounded-[2.5rem] p-6
        {type === 'primary' ? 'orange-glow' : ''}
        {type === 'catalog'
			? 'flex-col space-y-4 rounded-[2.5rem] border border-brand-orange/20 bg-brand-orange/10 p-8 text-center transition-all hover:bg-brand-orange/20'
			: ''}"
	>
		{#if type === 'catalog'}
			<div class="text-sm font-bold tracking-widest text-brand-orange uppercase">{description}</div>
			<h4 class="text-xl font-bold text-white">{title}</h4>
			<p class="text-sm text-slate-400">Cek produk & layanan kami lainnya di Berbagi.Link</p>
			<div
				class="flex items-center justify-center gap-2 rounded-2xl bg-brand-orange px-8 py-3 font-bold text-white shadow-lg shadow-brand-orange/20"
			>
				Akses Katalog Lengkap
			</div>
		{:else}
			{#if type === 'primary'}
				<div
					class="pointer-events-none absolute top-0 right-0 h-full w-32 bg-brand-orange/5 blur-3xl"
				></div>
			{/if}
			<div
				class="flex h-14 w-14 shrink-0 items-center justify-center rounded-2xl text-2xl transition-transform group-hover:scale-110
                {type === 'wa' ? 'bg-green-500/10' : ''}
                {type === 'discord' ? 'bg-indigo-500/10' : ''}
                {type === 'admin' ? 'bg-slate-800' : ''}"
			>
				{icon}
			</div>
			<div class="flex-1 text-left">
				<h3 class="text-lg font-bold text-white">{title}</h3>
				<p class="text-xs text-slate-400">{description}</p>
			</div>
			<div class="text-slate-600 transition-colors group-hover:text-brand-orange">
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
