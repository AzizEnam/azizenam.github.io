<script lang="ts">
  export let title: string;
  export let ogTitle: string | null = null;
  export let description: string;
</script>

<svelte:head>
  <title>{title}</title>
  <meta name="description" content={description} />
  <meta property="og:title" content={ogTitle ?? title} />
  <meta property="og:description" content={description} />
  <!--
    Optional social-share preview image. Drop a file in static/assets/images/
    and set its full URL here, then uncomment the two meta tags below.
  <meta property="og:image" content="https://azizenam.github.io/assets/images/og.jpg" />
  <meta name="twitter:card" content="summary_large_image" />
  -->
</svelte:head>
