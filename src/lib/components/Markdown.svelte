<script lang="ts">
	import { marked } from 'marked';
    import markedKatex from "marked-katex-extension";

	export let source: string;

	marked.use(markedKatex({ nonStandard: true }));

	$: html = marked.parse(source);
</script>

<link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/katex@0.13.11/dist/katex.min.css"
    integrity="sha384-Um5gpz1odJg5Z4HAmzPtgZKdTBHZdw8S29IecapCSB31ligYPhHQZMIlWLYQGVoc"
    crossOrigin="anonymous"
/>

<div class="md-output">
	{@html html}
</div>

<style lang="postcss">
	.md-output :global(p) {
		@apply mb-4 font-light;
	}

	.md-output :global(strong) {
		@apply font-semibold;
	}

	.md-output :global(code) {
		@apply text-[95%];
	}

	.md-output :global(a) {
		@apply underline underline-offset-[3px] decoration-neutral-400 dark:decoration-neutral-500;
		@apply hover:text-black hover:decoration-black transition-colors;
		@apply dark:hover:text-white dark:hover:decoration-white;
	}

	@reference "../../app.css";
</style>
