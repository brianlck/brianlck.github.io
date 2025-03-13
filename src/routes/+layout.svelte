<script lang="ts">
  import "../app.css";

  import Header from "$lib/components/Header.svelte";
  
  import type { LayoutData } from "./$types";
  export let data: LayoutData;

  
  import { browser } from "$app/environment";
  import { fly } from "svelte/transition";
  const isMobile = browser && /Android|iPhone/i.test(navigator.userAgent);
  const reducedMotion =
    browser && matchMedia("(prefers-reduced-motion: reduce)").matches;


  // ANIMATION CONSTANT
  const duration = 200;
  const flyOffset = 10;

</script>

<Header />

{#if isMobile || reducedMotion}
  <main>
    <slot />
  </main>
{:else}
  {#key data.pathname}
    <main
      in:fly={{ x: -flyOffset, duration, delay: duration }}
      out:fly={{ y: flyOffset, duration }}
    >
      <slot />
    </main>
  {/key}
{/if}

