<script lang="ts">
	const stats = [
		{ value: '10k+', label: 'Member Aktif' },
		{ value: '100%', label: 'Fokus Syariah' },
		{ value: '#1', label: 'Crypto Hub ID' }
	];
</script>

<section class="pt-8 text-center">
	<div class="flex flex-wrap justify-center gap-8 md:gap-12">
		{#each stats as stat, i}
			{#if i > 0}
				<div class="hidden border-r border-slate-800 md:block"></div>
			{/if}
			<div>
				<div class="text-2xl font-bold text-white">{stat.value}</div>
				<div class="text-xs uppercase tracking-tighter text-slate-500">{stat.label}</div>
			</div>
		{/each}
	</div>
</section>
