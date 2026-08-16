<script lang="ts">
  import Markdown from '$lib/components/Markdown.svelte';

  type Paper = {
    title: string;
    date: String;
    authors: string[];
    content: string;
    link: string;
    image: string;
  };

  export let data: Paper;
  export let images: any;
</script>

<div class="space-y-4">
  <h3 class="mb-2 text-xl font-semibold text-black flex items-center gap-2">
    <a class="link mr-1" href={data.link}>{data.title}</a>
    <small class="text-base font-normal whitespace-nowrap text-neutral-500">
      {data.date}
    </small>
  </h3>

  <p class="font-serif">
    <span class="g">With </span>
    {#each data.authors as author, i}
      {#if i < data.authors.length - 2}
        {author}<span class="g">,&nbsp;</span>
      {:else if i === data.authors.length - 2}
        {author}<span class="g">,&nbsp;and&nbsp;</span>
      {:else}
        {author}
      {/if}
    {/each}
  </p>
  <Markdown source={data.content} />

  <hr />
</div>