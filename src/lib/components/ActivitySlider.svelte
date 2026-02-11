<script lang="ts">
	import activity1 from '$lib/assets/activity-1.jpg';
	import activity2 from '$lib/assets/activity-2.jpg';
	import activity3 from '$lib/assets/activity-3.jpg';
	import activity4 from '$lib/assets/activity-4.jpg';
	import activity5 from '$lib/assets/activity-5.jpg';

	const images = [
		{ src: activity1, alt: 'Kegiatan CryptoSharia 1' },
		{ src: activity2, alt: 'Kegiatan CryptoSharia 2' },
		{ src: activity3, alt: 'Kegiatan CryptoSharia 3' },
		{ src: activity4, alt: 'Kegiatan CryptoSharia 4' },
		{ src: activity5, alt: 'Kegiatan CryptoSharia 5' }
	];
	let scrollContainer: HTMLDivElement;
	let currentIndex = $state(0);

	function handleScroll() {
		if (!scrollContainer) return;

		const containerCenter = scrollContainer.scrollLeft + scrollContainer.clientWidth / 2;
		const children = Array.from(scrollContainer.children);

		let closestIndex = 0;
		let minDistance = Infinity;

		children.forEach((child, i) => {
			const childCenter =
				(child as HTMLElement).offsetLeft + (child as HTMLElement).clientWidth / 2;
			const distance = Math.abs(containerCenter - childCenter);
			if (distance < minDistance) {
				minDistance = distance;
				closestIndex = i;
			}
		});

		currentIndex = closestIndex;
	}

	function scrollToImage(i: number) {
		if (!scrollContainer) return;
		const child = scrollContainer.children[i] as HTMLElement;
		if (!child) return;

		const targetScroll = child.offsetLeft - (scrollContainer.clientWidth - child.clientWidth) / 2;
		scrollContainer.scrollTo({ left: targetScroll, behavior: 'smooth' });
	}
</script>

<section class="space-y-6 pt-12">
	<div class="flex items-center justify-between px-2">
		<h3 class="text-gradient text-xl font-bold text-foreground">Kegiatan Kami</h3>
		<span class="text-[10px] font-medium tracking-widest text-faded uppercase"
			>Geser untuk lihat &rarr;</span
		>
	</div>

	<div class="relative">
		<div
			bind:this={scrollContainer}
			onscroll={handleScroll}
			class="no-scrollbar flex snap-x snap-mandatory gap-4 overflow-x-auto scroll-smooth pb-4"
			style="scrollbar-width: none; -ms-overflow-style: none;"
		>
			{#each images as image (image.src)}
				<div class="w-[85%] shrink-0 snap-center first:ml-2 last:mr-2 md:w-[60%]">
					<div class="glass-card aspect-video overflow-hidden rounded-[2.5rem] border-0">
						<img
							src={image.src}
							alt={image.alt}
							class="h-full w-full object-cover transition-transform duration-700 hover:scale-110"
							loading="lazy"
						/>
					</div>
				</div>
			{/each}
		</div>

		<!-- Indicators -->
		<div class="mt-4 flex justify-center gap-2">
			{#each images as image, i (image.src)}
				<button
					aria-label="Go to slide {i + 1}"
					onclick={() => scrollToImage(i)}
					class="h-1.5 cursor-pointer rounded-full transition-all duration-300
                    {currentIndex === i ? 'w-6 bg-primary' : 'w-1.5 bg-line'}"
				></button>
			{/each}
		</div>
	</div>
</section>

<style>
	.no-scrollbar::-webkit-scrollbar {
		display: none;
	}
</style>
