<script lang="ts">
  import { page } from "$app/stores";

  const links = [
    { name: "projects", href: "/projects" },
    { name: "resume", href: "/resume" },
  ];
</script>

<aside class="sidebar" data-sveltekit-preload-code="eager">
  <a href="/" class="inline-block">
    <img
      class="profile"
      src="/assets/images/profile.jpg"
      alt="Aziz Enam"
      width="128"
      height="128"
    />
  </a>

  <h1 class="mt-5 leading-tight">
    <a href="/" class="text-black font-bold text-2xl">Aziz Enam</a>
  </h1>
  <p class="text-neutral-500 mb-6">Robotics &amp; ML Engineer</p>

  <nav>
    {#each links as link (link.href)}
      <a
        href={link.href}
        class="navlink"
        class:active={$page.url.pathname === link.href}
      >
        {link.name}
      </a>
    {/each}
  </nav>

  <div class="social">
    <a class="link" href="https://twitter.com/sazizenam">@sazizenam</a>
    <a class="link" href="mailto:azizenam@gmail.com">azizenam@gmail.com</a>
  </div>
</aside>

<style lang="postcss">
  .sidebar {
    @apply self-start lg:sticky lg:top-12;
  }

  .profile {
    @apply h-32 w-32 rounded-full object-cover;
  }

  nav {
    @apply flex flex-col items-start gap-y-2 text-xl text-neutral-500 mb-8;
  }

  .navlink {
    @apply hover:text-black transition-colors;
  }

  .navlink.active {
    @apply text-black;
  }

  .social {
    @apply flex flex-col gap-y-1 text-base text-neutral-500;
  }
</style>
