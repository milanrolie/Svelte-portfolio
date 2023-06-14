<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to("#legends-marquee", {
      scrollTrigger: {
        trigger: "#legends-marquee",
        scrub: 1,
        start: "top-=1000",
        end: "bottom+=1000",
      },
      "--x": 1,
    });
  });
</script>

<section>
  <div class="sticky-marquee">
    <p id="legends-marquee">studio rolie studio rolie studio rolie</p>
  </div>
</section>

<style>
  section {
    position: sticky;
    top: 0;
    height: max-content;
    padding: 0;
    overflow-x: hidden;
  }

  .sticky-marquee {
    height: 50vh;
    background-color: rgb(103, 103, 103);
    z-index: -1;
    --x: 0;
    max-width: 100vw;
  }

  #legends-marquee {
    display: block;
    font-size: 7em;
    color: var(--bitterSweet);
    text-transform: uppercase;
    letter-spacing: 10px;
    font-family: "Outfit", sans-serif;
    white-space: nowrap;
    width: max-content;
    font-weight: 200;
    margin-bottom: 0%;
    transform: translateX(calc((-100% + 100vw) * var(--x)));
    padding-left: 4%;
  }
</style>
