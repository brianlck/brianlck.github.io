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
  <h3 class="mb-2 flex items-start justify-between gap-4 text-xl font-semibold text-black">
    <a class="link min-w-0" href={data.link}>
      {data.title}
    </a>

    <small class="shrink-0 whitespace-nowrap text-base font-normal text-neutral-500">
      {data.date}
    </small>
  </h3>

  <p class="font-serif">
    <span class="g">With </span>

    {#each data.authors as author, i}
      <span class="whitespace-nowrap">
        {author}{#if i < data.authors.length - 2}<span class="g">,&nbsp;</span>{:else if i === data.authors.length - 2}<span class="g">,&nbsp;and&nbsp;</span>{/if}
      </span>
    {/each}
  </p>

  <hr />
</div>