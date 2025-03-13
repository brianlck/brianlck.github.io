<script lang="ts">
	import Paper from './Paper.svelte';

	const papers = import.meta.glob('../../papers/*.md', {
		eager: true
	}) as Record<string, any>;
	const images = import.meta.glob('../../papers/*.{png,jpg,svg}', {
		eager: true
	}) as any;

</script>

<div class="descriptor layout-md mb-12 text-xl leading-tight text-black">
	<span class="g">@ </span> Publications
	<hr class="mt-5" />
</div>

<div class="layout-md font-seif space-y-10 text-lg">

	<div class="space-y-10">
		{#each Object.entries(papers) as [_, paper]}
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
