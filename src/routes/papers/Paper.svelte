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
  <h3
    class="mb-2 grid w-full grid-cols-[minmax(0,1fr)_auto] items-start gap-4 text-xl font-semibold text-black"
  >
    <a class="link min-w-0" href={data.link}>
      {data.title}
    </a>

    <small
      class="whitespace-nowrap text-right text-base font-normal text-neutral-500"
    >
      {data.date}
    </small>
  </h3>

  <p class="font-serif">
    <span class="g">With </span>    
     {#each data.authors as author, i}
      {#if i < data.authors.length - 2}
        <span class="whitespace-nowrap">
          {author}<span class="g">,</span>
        </span>{' '}
      {:else if i === data.authors.length - 2}
        <span class="whitespace-nowrap">
          {author}<span class="g">,</span>
        </span>{' '}
        <span class="whitespace-nowrap">
          <span class="g">and&nbsp;</span>{data.authors[i + 1]}
        </span>
      {/if}
    {/each}
  </p>

  <hr />
</div>