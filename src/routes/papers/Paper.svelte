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

  {#if data.image}
    {#if data.image.endsWith('.mp4')}
      <video
        src={images[`../../papers/${data.image}`]?.default}
        autoplay
        loop
        muted
        playsinline
        class="mx-auto max-h-96 rounded-lg"
      >
        Your browser does not support the video tag.
      </video>
    {:else}
      <img
        src={images[`../../papers/${data.image}`]?.default}
        alt="{data.title} preview image"
        class="mx-auto max-h-96"
      />
    {/if}
  {/if}

  <hr />
</div>