<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import HubLink from '$lib/components/HubLink.svelte';
	import SocialProof from '$lib/components/SocialProof.svelte';
	import FAQ from '$lib/components/FAQ.svelte';
</script>

<main class="mx-auto w-full max-w-xl space-y-8 px-5 py-12 md:py-20">
	<Hero
		title="Satu Pintu Masuk ke <br> <span class='text-brand-orange'>Ekosistem Kami.</span>"
		subtitle="Berhenti investasi sendirian. Navigasi market crypto dengan komunitas yang memprioritaskan keberkahan dan kaidah syariah."
	/>

	<div class="space-y-4">
		<HubLink
			href="https://wa.me/your-link"
			title="Grup WA Komunitas"
			description="Diskusi harian & update pasar gratis."
			icon="💬"
			type="wa"
		/>

		<HubLink
			href="https://discord.gg/your-link"
			title="Discord Forum"
			description="Riset mendalam & library edukasi."
			icon="👾"
			type="discord"
		/>

		<HubLink
			href="https://wa.me/admin"
			title="Hubungi Admin"
			description="Bantuan & pertanyaan umum."
			icon="👨‍💻"
			type="admin"
		/>

		<div class="pt-4">
			<HubLink
				href="https://berbagi.link/cryptosharia"
				title="Lihat Semua Layanan"
				description="Premium Tools & Catalog"
				type="catalog"
			/>
		</div>
	</div>

	<SocialProof />

	<FAQ />

	<footer class="space-y-4 pt-20 pb-10 text-center">
		<div class="flex justify-center gap-4 text-xs text-slate-500">
			<a href="/syarat-ketentuan" class="transition-colors hover:text-brand-orange"
				>Syarat & Ketentuan</a
			>
			<span>•</span>
			<a href="/kebijakan-privasi" class="transition-colors hover:text-brand-orange"
				>Kebijakan Privasi</a
			>
		</div>
		<p class="mx-auto max-w-xs text-[10px] text-slate-600">
			© 2026 CryptoSharia Hub. Investasi crypto memiliki risiko tinggi. Pastikan kamu memahami aset
			yang kamu beli.
		</p>
	</footer>
</main>
