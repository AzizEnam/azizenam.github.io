<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import Workplace from "./Workplace.svelte";
</script>

<Seo
  title="Aziz Enam – Resume"
  description="Robotics and machine learning engineer. Autonomy, perception, localization, calibration, and mapping."
/>

<section class="layout-md pt-12 pb-2">
  <p>
    <a class="link" rel="external" href="/assets/pdf/Aziz_Enam_Resume.pdf"
      >Download a PDF version</a
    >.
  </p>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Experience</h2>

  <Workplace
    title="Founding Member of Technical Staff"
    company="Alquist"
    url="https://www.alquistrobotics.com/"
    dates="May 2025 – Current"
    location="New York, NY"
  >
    <svelte:fragment slot="description">
      Architect, technical owner, and solo developer of an end-to-end onboard
      autonomous navigation stack for next-generation robotic platforms.
    </svelte:fragment>
    <li>
      Architected and deployed a vision-only autonomy pipeline spanning
      perception, localization, planning, and control.
    </li>
    <li>
      Deployed the onboard navigation stack on the NVIDIA Jetson Orin embedded
      platform, achieving sub-100&nbsp;ms end-to-end latency from camera
      exposure to commanded velocity. The real-time pipeline integrated
      visual-inertial odometry (VIO), learned depth inference, truncated and
      Euclidean signed-distance field (TSDF/ESDF) mapping, wavefront cost maps,
      and a sampling-based model predictive control (MPC) policy.
    </li>
    <li>
      Developed a scalable automatic end-to-end metric 3D reconstruction
      pipeline for sensor calibration and generation of onboard localization
      maps. Engineered the system to operate robustly in sparse-feature
      environments, including warehouses and retail stores, enabling
      reconstruction of 50,000+ sq ft facilities and delivery of
      localization-ready artifacts within hours.
    </li>
  </Workplace>

  <Workplace
    title="Senior Applied Scientist — Localization, Calibration & Mapping"
    company="Cruise"
    url="https://www.getcruise.com/"
    dates="January 2020 – November 2024"
    location="San Francisco, CA"
  >
    <svelte:fragment slot="description">
      Core engineer of the Localization, Calibration and Mapping team,
      responsible for all things related to sensor intrinsic and extrinsic
      calibrations. Promoted from ML/Robotics Software Engineer to Senior
      Applied Scientist in July 2022.
    </svelte:fragment>
    <li>
      Solo and joint inventor on
      <a
        class="link"
        href="https://patents.google.com/?inventor=Syed+Aziz+Enam&assignee=GM+Cruise+Holdings+LLC.&country=US&num=25"
        >multiple patents</a
      > related to sensor calibration.
    </li>
    <li>
      Co-developed and researched a fully automated calibration system for
      diverse sensors, including cameras, lidar, radar, and IMUs, in
      unstructured environments. This system achieves complete calibration of
      new vehicles within 1 mile of driving in parking lots or garages.
    </li>
    <li>
      Authored and maintained online calibration monitors designed to track the
      gradual drift of extrinsic calibrations in vehicles and perform updates
      when deemed safe.
    </li>
  </Workplace>

  <Workplace
    title="Software Engineer — Computer Vision"
    company="Postmates X (Serve Robotics)"
    url="https://www.serverobotics.com/"
    dates="January 2018 – December 2020"
    location="San Francisco, CA"
  >
    <svelte:fragment slot="description">
      Core engineer of an early-stage team for Postmates' autonomous rover
      project,
      <a
        class="link"
        href="https://www.forbes.com/sites/lanabandoim/2018/12/21/postmates-reveals-its-autonomous-delivery-rover-called-serve/"
        >Serve</a
      >.
    </svelte:fragment>
    <li>
      Designed processes to calibrate cameras with lidar for sensor fusion,
      along with visualization tools and quality metrics.
    </li>
    <li>
      Developed and deployed deep learning systems for object detection and
      scene segmentation.
    </li>
  </Workplace>

  <Workplace
    title="Software Engineer — Machine Learning"
    company="FirstRain"
    dates="August 2016 – July 2017"
    location="San Mateo, CA"
    hiddenMode="click"
  >
    <li>
      Worked on algorithms to remove and filter content from FirstRain's corpus
      that was not considered business relevant.
    </li>
  </Workplace>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Patents</h2>

  <p class="mb-4">
    Solo and joint inventor on patents related to autonomous-vehicle sensor
    calibration, assigned to GM Cruise Holdings.
    <a
      class="link"
      href="https://patents.google.com/?inventor=Syed+Aziz+Enam&assignee=GM+Cruise+Holdings+LLC.&country=US&num=25"
      >View all on Google Patents.</a
    >
  </p>

  <ul class="patents">
    <li>
      <a class="link" href="https://patents.google.com/patent/US12522223B2"
        >Map-assisted target detection for sensor calibration</a
      >
      <span class="meta">US 12,522,223 B2 · 2026</span>
      <span class="pdesc"
        >Extrinsically calibrates and checks autonomous-vehicle sensors on-road
        by matching live sensor returns against static objects identified from a
        semantic map layer.</span
      >
    </li>
    <li>
      <a class="link" href="https://patents.google.com/patent/US12386057B2"
        >Continuous radar calibration check</a
      >
      <span class="meta">US 12,386,057 B2 · 2025</span>
      <span class="pdesc"
        >Continuously monitors radar-to-lidar alignment by tracking relative
        object positions over time, flagging the system as out of calibration
        and triggering corrective action when drift exceeds a threshold.</span
      >
    </li>
    <li>
      <a class="link" href="https://patents.google.com/patent/US12221119B2"
        >Drive-through calibration process</a
      >
      <span class="meta">US 12,221,119 B2 · 2025</span>
      <span class="pdesc"
        >Validates a vehicle's sensor calibration by driving through an
        environment mapped with a series of known targets, confirming the
        extrinsic parameters between sensors stay within bounds before
        autonomous operation.</span
      >
    </li>
  </ul>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Skills</h2>

  <div class="mb-4">
    <h3 class="font-medium mb-1">Scientific Computing:</h3>
    <p>
      C++17, Python, PyTorch / TensorFlow / TensorRT, OpenCV, PCL, Eigen, Ceres,
      scikit-learn, NumPy / SciPy, CUDA
    </p>
  </div>

  <div class="mb-4">
    <h3 class="font-medium mb-1">Robotics:</h3>
    <p>
      ROS, Linear Algebra, Convex Optimization, State Estimation, Deep Learning,
      Optical Flow, Sensor Calibration, SLAM, Kalman Filters, Model Predictive
      Control, 3DGS
    </p>
  </div>
</section>

<section class="layout-md py-12">
  <h2 class="heading2">Education</h2>

  <div class="mb-4">
    <div class="flex justify-between items-end">
      <h3 class="text-black text-lg">University of California, Irvine</h3>
      <div class="text-neutral-500 mb-0.5">2014 — 2016</div>
    </div>
    <p class="byline">M.S. in Applied Mathematics</p>
  </div>

  <div class="mb-4">
    <div class="flex justify-between items-end">
      <h3 class="text-black text-lg">University of California, San Diego</h3>
      <div class="text-neutral-500 mb-0.5">2010 — 2014</div>
    </div>
    <p class="byline">B.S. in Electrical Engineering and Mathematics</p>
  </div>
</section>

<style lang="postcss">
  .byline {
    @apply font-serif italic;
  }

  .patents {
    @apply list-disc pl-7 marker:text-neutral-400 space-y-3;
  }

  .patents .meta {
    @apply block text-neutral-500 text-base;
  }

  .patents .pdesc {
    @apply block text-base mt-0.5;
  }
</style>
