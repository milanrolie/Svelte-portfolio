<script>
import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".transition", {
      y: '-110%',
      rotate: 0,
      duration: 1,
    });
});

</script>

<div class="transition"></div>

<style>
    .transition {
        position: fixed;
        top: 0;
        left: -10%;
        height: 120vh;
        width: 120%;
        background-color: var(--dark);
        z-index: 300;
        /* transform: translateY(100%) rotate(-10deg); */
    }
</style>