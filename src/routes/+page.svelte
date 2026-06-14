<script lang="ts">
  import { ArrowUpRight } from "lucide-svelte";

  import Seo from "$lib/components/Seo.svelte";

  // Edit this list to highlight your own work. Each `href` points to an
  // anchor on the /projects page (the id is the project's file name).
  const featuredProjects = [
    {
      name: "Example Project",
      href: "/projects#example-project",
      desc: "a short description of a project you want to feature",
      aside: "optional note, e.g. an award or stat",
    },
  ];
</script>

<Seo title="Aziz Enam" description="Personal website." />

<div class="layout-md text-lg space-y-14">
  <div class="space-y-5">
    <p>
      Hi, I'm Aziz. Write a short introduction about yourself here — what you
      do, what you're working on, and what you care about.
    </p>

    <p>
      You can use <em>emphasis</em> like this to call out themes that matter to
      you, and add links to <a class="link" href="/">things you've made</a>.
    </p>
  </div>

  <div class="leading-snug space-y-4">
    <p class="pb-2">Featured work:</p>

    {#each featuredProjects as project}
      <a class="project-pair" href={project.href}>
        <div class="text-black font-medium">
          {project.name}
          <ArrowUpRight size={18} class="inline text-neutral-400" />
        </div>
        <div>
          <p>{project.desc}</p>
          {#if project.aside}
            <aside>{project.aside}</aside>
          {/if}
        </div>
      </a>
    {/each}
  </div>

  <div class="space-y-5">
    <p>
      Add more paragraphs here — your background, previous work, interests, and
      anything else you'd like visitors to know.
    </p>

    <p>Other interests: add a few here.</p>
  </div>
</div>

<style lang="postcss">
  em {
    @apply font-serif text-[110%] leading-[100%];
  }

  .project-pair {
    @apply grid sm:grid-cols-[1fr,2fr] gap-y-1 -mx-3 px-3 py-2 hover:bg-neutral-100 transition-colors;
  }

  aside {
    @apply mt-0.5 text-base text-neutral-500;
  }
</style>
