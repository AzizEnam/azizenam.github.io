<script lang="ts">
  import { fade } from "svelte/transition";

  export let title: string;
  export let company: string;
  export let url: string | undefined = undefined;
  export let dates: string;
  export let location: string;
  export let hiddenMode: "click" | "always" | undefined = undefined;

  let hidden = hiddenMode === "click";
</script>

{#if hiddenMode !== "always"}
  <div
    class="my-10"
    class:cursor-pointer={hidden}
    on:click={() => (hidden = false)}
    on:keypress={() => {}}
  >
    <h3 class="text-black text-lg leading-tight mb-1">
      {title} at
      {#if url}
        <a class="link" href={url}>{company}</a>
      {:else}
        {company}
      {/if}
    </h3>
    <p class="font-light mb-2">
      <span class="whitespace-nowrap">{dates}</span>
      <span class="px-0.5 text-neutral-500">•</span>
      <span class="whitespace-nowrap">{location}</span>
    </p>
    {#if !hidden}
      <div in:fade|local>
        {#if $$slots.description}
          <p class="mb-2"><slot name="description" /></p>
        {/if}
        <ul class="list-disc pl-7 marker:text-neutral-400 space-y-1">
          <slot />
        </ul>
      </div>
    {/if}
  </div>
{/if}
