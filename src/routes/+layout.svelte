<script lang="ts">
  import "@fontsource/newsreader/400-italic.css";
  import "../app.css";

  import { browser } from "$app/environment";

  import { fly } from "svelte/transition";

  import Sidebar from "$lib/components/Sidebar.svelte";
  import type { LayoutData } from "./$types";

  export let data: LayoutData;

  const isMobile = browser && /Android|iPhone/i.test(navigator.userAgent);
  const reducedMotion =
    browser && matchMedia("(prefers-reduced-motion: reduce)").matches;
</script>

<!--
  To add analytics, put your provider's snippet inside a <svelte:head> block
  here (wrap it in `{#if !dev}` so it only runs in production).
-->

<div class="shell">
  <Sidebar />

  {#if isMobile || reducedMotion}
    <!--
      Disable page transitions on mobile due to a browser engine bug.
      Also disable them for reduced-motion users.
    -->
    <main>
      <slot />
    </main>
  {:else}
    {#key data.pathname}
      <main
        in:fly={{ x: -10, duration: 350, delay: 350 }}
        out:fly={{ y: 5, duration: 350 }}
      >
        <slot />
      </main>
    {/key}
  {/if}
</div>

<style lang="postcss">
  .shell {
    @apply mx-auto max-w-[1140px] px-5 sm:px-8;
    @apply lg:grid lg:grid-cols-[228px,1fr] lg:gap-x-16;
  }

  /* Space between the stacked sidebar and content on mobile. */
  main {
    @apply mt-12 lg:mt-0 min-w-0;
  }
</style>
