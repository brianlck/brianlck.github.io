<script lang="ts">
    export let title: string;
    export let description: string;
</script>

<svelte:head>
    <title>{title}</title>
    <meta name="description" content={description} />
    <meta property="og:title" content={title} />
    <meta property="og:description" content={description} />
    <meta property="og:image" content="/assets/photo.jpg" />
</svelte:head>