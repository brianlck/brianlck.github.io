<script lang="ts">
	import Metadata from '$lib/components/Metadata.svelte';
	import Paper from './Paper.svelte';

	const papers = import.meta.glob('../../papers/*.md', {
		eager: true
	}) as Record<string, any>;
	
	const images = import.meta.glob('../../papers/*.{png,jpg,svg,mp4}', {
		eager: true
	}) as any;

	const monthMap: Record<string, number> = {
		Jan: 0, Feb: 1, Mar: 2, Apr: 3, May: 4, Jun: 5,
		Jul: 6, Aug: 7, Sep: 8, Oct: 9, Nov: 10, Dec: 11
	};

	const sortedPapers = Object.entries(papers).sort(([_a, a], [_b, b]) => {
		const [monthA, yearA] = a.date.split(' ');
		const [monthB, yearB] = b.date.split(' ');

		const yearDiff = parseInt(yearB) - parseInt(yearA);

		if (yearDiff !== 0) return yearDiff;
		return monthMap[monthB] - monthMap[monthA];
	});
</script>

<Metadata title="Brian Lee" description="Papers by Brian Lee" />

<div class="descriptor layout mb-12 text-xl leading-tight text-black">
	<span class="g">@ </span> Publications
	<hr class="mt-5" />
</div>

<div class="layout font-seif space-y-10 text-lg">
	<div class="space-y-10">
		{#each sortedPapers as paper}
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
