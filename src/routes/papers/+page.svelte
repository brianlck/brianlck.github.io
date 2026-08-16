<script lang="ts">
	import Metadata from '$lib/components/Metadata.svelte';
	import Paper from './Paper.svelte';

	// Import all markdown files and assets
	const papers = import.meta.glob('../../papers/*.md', {
		eager: true
	}) as Record<string, any>;
	
	const images = import.meta.glob('../../papers/*.{png,jpg,svg,mp4}', {
		eager: true
	}) as any;

	// Month lookup for Safari-safe parsing
	const monthMap: Record<string, number> = {
		Jan: 0, Feb: 1, Mar: 2, Apr: 3, May: 4, Jun: 5,
		Jul: 6, Aug: 7, Sep: 8, Oct: 9, Nov: 10, Dec: 11
	};

	// Convert object to array and sort by date descending
	const sortedPapers = Object.entries(papers).sort(([_a, a], [_b, b]) => {
		// Extract date strings (assumes format "Jan 2026")
		const dateStrA = a.date || "";
		const dateStrB = b.date || "";

		const [mA, yA] = dateStrA.split(' ');
		const [mB, yB] = dateStrB.split(' ');

		// Convert years to numbers for comparison
		const yearA = parseInt(yA);
		const yearB = parseInt(yB);

		// 1. Sort by Year first
		if (yearB !== yearA) {
			return yearB - yearA;
		}

		// 2. If years are equal, sort by month index
		return (monthMap[mB] ?? 0) - (monthMap[mA] ?? 0);
	});
</script>

<Metadata title="Brian Lee" description="Papers by Brian Lee" />

<div class="descriptor layout mb-12 text-xl leading-tight text-black">
	<span class="g">@ </span> Publications
	<hr class="mt-5" />
</div>

<div class="layout font-serif space-y-10 text-lg">
	<div class="space-y-10">
		{#each sortedPapers as [_, paper]}
			<Paper data={paper} {images} />
		{/each}
	</div>
</div>

<style lang="postcss">
	.descriptor {
		font-family: Merriweather, serif;
	}

	@reference "../../app.css";
</style>
