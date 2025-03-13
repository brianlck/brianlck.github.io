<script lang="ts">
    import { page } from "$app/stores";
  
    const links = [
      { name: "Papers", href: "/papers" },
    ];
  
    let pageTitle: string | null = null;
    $: {
      const link = links.find(({ href }) => href === $page.url.pathname);
      pageTitle = link?.name || null;
    }
  </script>
  
  <header
    class="layout-md flex justify-between items-start"
    data-sveltekit-noscroll
    data-sveltekit-preload-code="eager"
  >
    <h1 class="font-bold text-black text-2xl mb-6">
      <a href="/">Lee Cheuk-Kit<span class="font-light text-neutral-400 text-[110%] ml-2 font-serif"> Brian </span></a>
    </h1>
    <nav>
      {#each links as link (link)}
        <a
          href={link.href}
          class="hover:text-black transition-colors"
          class:text-black={$page.url.pathname === link.href}
        >
          {link.name}
        </a>
      {/each}
    </nav>
  </header>
  
  <style lang="postcss">

    nav {
      @apply flex items-start text-neutral-500 justify-end space-x-6 text-lg py-0.5;
    }
  
    @media (max-width: 420px) {
      nav {
        @apply flex-col items-end space-x-0;
      }
    }

    @reference "../../app.css";
  </style>
  