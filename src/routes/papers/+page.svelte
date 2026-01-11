<script lang="ts">
	import Metadata from '$lib/components/Metadata.svelte';
	import Paper from './Paper.svelte';

	const papersRaw = import.meta.glob('../../papers/*.md', {
		eager: true
	}) as Record<string, any>;
	
	const images = import.meta.glob('../../papers/*.{png,jpg,svg,mp4}', {
		eager: true
	}) as any;

	const sortedPapers = Object.values(papersRaw).sort((a, b) => {
		const dateA = new Date(a.date || 0).getTime();
		const dateB = new Date(b.date || 0).getTime();
		return dateB - dateA;
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
