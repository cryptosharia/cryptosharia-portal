<script>
	import Hero from '$lib/components/Hero.svelte';
	import HubLink from '$lib/components/HubLink.svelte';
	import SocialProof from '$lib/components/SocialProof.svelte';
	import FAQ from '$lib/components/FAQ.svelte';
	import ActivitySlider from '$lib/components/ActivitySlider.svelte';
</script>

<main class="mx-auto w-full max-w-xl space-y-8 px-5 py-12 md:py-20">
	<Hero
		title="Platform Ekosistem<br>Kripto Syariah<br><span class='text-primary'>Terbesar di Indonesia.</span>"
		subtitle="Wadah belajar dan komunitas Muslim untuk menavigasi dunia Web3 serta crypto dengan prinsip syariah yang aman, transparan, dan terarah."
	/>

	<div class="space-y-4">
		<HubLink
			href="https://chat.whatsapp.com/EkyYn2gmXVN7tspbMvz6fx"
			title="Grup WA Komunitas Gratis"
			description="Diskusi harian & update pasar gratis."
			icon="💬"
			type="wa"
		/>

		<HubLink
			href="https://discord.gg/raBFJtB4ja"
			title="Grup Discord Gratis"
			description="Riset mendalam & library edukasi."
			icon="👾"
			type="discord"
		/>

		<HubLink
			href="https://wa.me/6282186584279?text={encodeURIComponent(
				"Assalamu'alaikum min, mau nanya terkait ..."
			)}"
			title="Join Member Premium"
			description="Hubungi admin CryptoSharia segera"
			icon="👨‍💻"
			type="admin"
		/>

		<div class="pt-4">
			<HubLink
				href="https://berbagi.link/cryptosharia"
				title="Katalog Produk dan Layanan"
				description="Gabung ke Discord Premium Crypto Syariah dan rasakan komunitas eksklusif yang dibimbing langsung oleh mentor-mentor handal yang siap membimbing kamu dari nol sampai paham strategi."
				type="catalog"
			/>
		</div>
	</div>

	<SocialProof />

	<ActivitySlider />

	<FAQ />

	<footer class="space-y-4 pt-20 pb-10 text-center">
		<!-- <div class="flex justify-center gap-4 text-xs text-slate-500">
			<a href="/syarat-ketentuan" class="transition-colors hover:text-brand-orange"
				>Syarat & Ketentuan</a
			>
			<span>•</span>
			<a href="/kebijakan-privasi" class="transition-colors hover:text-brand-orange"
				>Kebijakan Privasi</a
			>
		</div> -->
		<p class="mx-auto max-w-xs text-[10px] text-slate-600">
			© 2025 - 2026 CryptoSharia. All rights reserved.
		</p>
	</footer>
</main>
