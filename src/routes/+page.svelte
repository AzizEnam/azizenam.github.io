<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
</script>

<Seo
  title="Aziz Enam"
  description="A builder in robotics and computer vision based in New York."
/>

<div class="layout-md text-lg space-y-5">
  <p>
    I'm a <em>builder</em> in robotics and computer vision based in New York.
  </p>

  <p>
    I'm currently a founding member of technical staff at
    <a class="link" href="https://www.alquistrobotics.com/">Alquist</a> working
    on vision-based autonomous navigation. Before that, I spent nearly five
    years at <a class="link" href="https://www.getcruise.com/">Cruise</a> as a
    senior applied scientist on the localization, calibration, and mapping team,
    and earlier built computer-vision systems for Postmates' Serve delivery
    robots. I'm named on several
    <a
      class="link"
      href="https://patents.google.com/?inventor=Syed+Aziz+Enam&assignee=GM+Cruise+Holdings+LLC.&country=US&num=25"
      >patents</a
    > in autonomous-vehicle sensor calibration.
  </p>

  <p>
    Take a look at my <a class="link" href="/resume">resume</a>, or reach me at
    <a class="link" href="mailto:azizenam@gmail.com">azizenam@gmail.com</a>.
  </p>
</div>

<style lang="postcss">
  em {
    @apply font-serif text-[110%] leading-[100%];
  }
</style>
