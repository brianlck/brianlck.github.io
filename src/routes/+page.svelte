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
		<p>I am building a new research lab.</p>

	    <p>Before this, a stint at Jane Street brought me home to Hong Kong.</p>
	
	    <p>At Harvard and Cambridge, I worked on the theory of generative modeling.</p>
	
	    <p>Cambridge is also where I completed my undergraduate studies.</p>
	
	    <p>These days, you can find me in Hong Kong, London, or San Francisco.</p>
		
		<p>Feel free to reach out at <a class="link" href="mailto:brianlee.lck@gmail.com">brianlee.lck@gmail.com</a>.</p>
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
