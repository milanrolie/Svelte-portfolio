<script>
import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".transition", {
      y: '-100%',
      delay: 0,
      stagger: 0,
      duration: 3,
    });
});

</script>

<div class="transition"></div>

<style>
    .transition {
        position: absolute;
        top: 0;
        height: 100vh;
        width: 100%;
        background-color: var(--dark);
        z-index: 300;
        /* transform: translateY(0); */
    }
</style>