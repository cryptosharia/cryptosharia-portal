<script lang="ts">
	let showAll = $state(false);

	const faqs = [
		{
			q: 'Apa saja manfaat bergabung di komunitas gratis?',
			a: `Dengan bergabung, Anda akan:
• **Berinteraksi langsung** dengan sesama investor Muslim.
• Mendapatkan **update pasar** yang aktual dan relevan.
• Info eksklusif seputar **webinar & event** edukatif.
• Kuis berhadiah dan program komunitas lainnya.`
		},
		{
			q: 'Apakah terbuka untuk pemula dan non-Muslim?',
			a: `**Ya, terbuka untuk semua.** Baik pemula maupun berpengalaman, dan tidak terbatas untuk Muslim. Namun, semua diskusi tetap berlandaskan **prinsip & etika syariah Islam**.`
		},
		{
			q: 'Apa perbedaan grup Gratis vs Premium?',
			a: `Grup Gratis fokus pada **literasi & networking**. 
Grup Premium memberikan **pendampingan intensif**, akses materi eksklusif, dan konsultasi syariah langsung dengan mentor berpengalaman.`
		},
		{
			q: 'Apakah memberikan sinyal trading?',
			a: `Fokus utama kami adalah **edukasi dan manajemen risiko**. Kami tidak memberikan sinyal instan. Di grup Premium, analisis pasar dibahas lebih mendalam namun tetap berbasis edukasi.`
		},
		{
			q: 'Apakah bergabung menjamin profit?',
			a: `**Tidak.** Tidak ada jaminan profit dalam investasi kripto. Komunitas ini bertujuan meminimalisir risiko melalui strategi dan disiplin yang benar.`
		},
		{
			q: 'Apakah membahas hukum kripto dalam Islam?',
			a: `**Ya.** Kami fokus pada aspek fikih muamalah, membahas isu **Gharar, Maysir, dan Riba** secara ilmiah merujuk pada pendapat ulama.`
		},
		{
			q: 'Apakah harus memiliki modal besar?',
			a: `**Tidak.** Siapa pun bisa bergabung bahkan jika masih tahap belajar tanpa modal. Memahami mekanisme pasar jauh lebih penting dibanding modal besar.`
		},
		{
			q: 'Apakah cocok untuk investasi jangka panjang?',
			a: `**Sangat cocok.** Literasi kripto bukan proses instan. Kami membangun komunitas agar Anda mampu berpikir kritis dan tidak terjebak *hype* sesaat.`
		}
	];

	const displayedFaqs = $derived(showAll ? faqs : faqs.slice(0, 4));
</script>

<section class="space-y-6 pt-12">
	<h3 class="text-gradient text-center text-xl font-bold">FAQ</h3>

	<div class="space-y-3">
		{#each displayedFaqs as faq (faq.q)}
			<details class="glass-card group overflow-hidden rounded-3xl p-0 transition-all">
				<summary
					class="flex cursor-pointer list-none items-center justify-between p-6 text-sm font-semibold transition-colors group-open:text-primary"
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
				<div class="whitespace-pre-line px-6 pb-6 text-sm leading-relaxed text-faded">
					{@html faq.a.replace(/\*\*(.*?)\*\*/g, '<strong class="text-foreground">$1</strong>')}
				</div>
			</details>
		{/each}
	</div>

	{#if faqs.length > 4}
		<div class="flex justify-center pt-2">
			<button
				onclick={() => (showAll = !showAll)}
				class="group flex cursor-pointer items-center gap-2 text-xs font-bold tracking-widest text-faded uppercase transition-colors hover:text-primary"
			>
				{showAll ? 'Lihat Lebih Sedikit' : 'Lihat Semua FAQ'}
				<svg
					class="h-4 w-4 transition-transform {showAll ? 'rotate-180' : ''}"
					fill="none"
					stroke="currentColor"
					viewBox="0 0 24 24"
				>
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"
					></path>
				</svg>
			</button>
		</div>
	{/if}
</section>

<style>
	/* details summary::-webkit-details-marker { display: none; } is handled by Tailwind's list-none */
</style>
