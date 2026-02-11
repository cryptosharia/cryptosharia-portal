<script lang="ts">
	const stats = [
		{ value: '2500+', label: 'Member Aktif' },
		{ value: '100%', label: 'Sesuai Syariah' },
		{ value: '15+', label: 'Partnership' }
	];
</script>

<section class="pt-8 text-center">
	<div class="flex flex-wrap justify-center gap-8 md:gap-12">
		{#each stats as stat, i (stat.label)}
			{#if i > 0}
				<div class="hidden border-r border-line md:block"></div>
			{/if}
			<div>
				<div class="text-2xl font-bold text-primary">{stat.value}</div>
				<div class="text-xs tracking-tighter text-faded uppercase">{stat.label}</div>
			</div>
		{/each}
	</div>
</section>
