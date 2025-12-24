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
		<p>I currently work at Jane Street. Previously, I was a researcher at Harvard and Cambridge, focused on projects with Michael Albergo and Francisco Vargas (2025). I hold an undergraduate degree from the University of Cambridge (2021–2024)</p>

		<p> My interests lie in the application of mathematical and computational frameworks to practical, real-world problems. </p>

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
