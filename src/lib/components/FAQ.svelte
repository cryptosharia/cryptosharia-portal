<script lang="ts">
	const faqs = [
		{
			q: 'Apa bedanya Hub ini dengan BerbagiLink?',
			a: 'Hub ini adalah pintu masuk utama (Gateway) untuk komunitas gratis. Sementara BerbagiLink adalah katalog lengkap untuk produk berbayar dan layanan teknis kami.'
		},
		{
			q: 'Apakah diskusi di komunitas berbayar?',
			a: 'Grup WhatsApp dan Area Publik Discord 100% gratis. Kami percaya edukasi dasar syariah harus bisa diakses semua orang tanpa hambatan biaya.'
		}
	];
</script>

<section class="space-y-6 pt-12">
	<h3 class="text-gradient text-center text-xl font-bold">Pertanyaan Umum</h3>
	<div class="space-y-3">
		{#each faqs as faq}
			<details class="glass-card group overflow-hidden rounded-3xl p-0 transition-all">
				<summary
					class="flex cursor-pointer list-none items-center justify-between p-6 font-semibold transition-colors group-open:text-brand-orange"
				>
					{faq.q}
					<svg
						class="h-5 w-5 transition-transform group-open:rotate-180"
						fill="none"
						stroke="currentColor"
						viewBox="0 0 24 24"
					>
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"
						></path>
					</svg>
				</summary>
				<div class="px-6 pb-6 text-sm leading-relaxed text-slate-400">
					{faq.a}
				</div>
			</details>
		{/each}
	</div>
</section>

<style>
	/* details summary::-webkit-details-marker { display: none; } is handled by Tailwind's list-none */
</style>
