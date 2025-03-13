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
	<p>
		Once upon a time, there were plans to feature non-academic works. However, life happened, and
		those ideas now linger in the realm of "what might have been."
	</p>

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
