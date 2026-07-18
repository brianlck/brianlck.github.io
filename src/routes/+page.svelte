<script>
	import Metadata from '$lib/components/Metadata.svelte';
</script>

<Metadata title="Brian Lee" description="Brian Lee Cheuk-Kit – Software Engineer and Researcher" />

<div class="descriptor layout mb-12 text-xl leading-tight text-black">
	<span class="g"> A </span> Software Engineer <span class="g"> and </span> Researcher
	<hr class="mt-5" />
</div>

<div class="layout font-light space-y-14 text-lg">
    <div class="space-y-5">
        <p> I am working on a new research lab. </p>
        <p> Prior to this, I was at Harvard working on the theory of generative modeling, following my undergraduate studies at Cambridge. </p>
        <p> I also spent a year working in Hong Kong, my hometown, working at Jane Street. </p>
        <p> Depending on the time of the year, I can be found in Hong Kong, London, or San Francisco. </p>
        <p> Feel free to reach out at <a class="link" href="mailto:brianlee.lck@gmail.com">brianlee.lck@gmail.com</a>. </p>
    </div>

	<div class="space-y-5">
		<img alt="Brian Lee sitting on a bench in Richmond" src="/assets/photo.jpg" />
		<p class="text-center text-sm text-neutral-500">
			A bench at Richmond, London. The dialogue references the 1979 film "Life of Brian"
		</p>
	</div>
</div>

<style lang="postcss">
	.descriptor {
		font-family: Merriweather, serif;
	}

	@reference "../app.css";
</style>
