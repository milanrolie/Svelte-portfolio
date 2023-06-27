<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".words", {
      scrollTrigger: {
        trigger: ".hero-wrapper",
        // pin: true,
        scrub: 1,
        start: "top+=20",
        end: "center+=200",
        // markers: true,
      },
      y: -150,
      // x: 20,
      // stagger: .2,
    });    

    gsap.from(".words", {
      y: 200,
      // stagger: .3,
      delay: 1,
      duration: 1.5,
      ease: "power4.out",
    });

  });
</script>

<section class="hero-wrapper">
  <h1>
    <div class="creative inline-block"><span class="words">creative</span></div>
    <div class="developer inline-block"><span class="words">developer &</span></div>
    <div class="designer inline-block"><span class="words">designer</span></div>
  </h1>
  <!-- <div class="info-wrapper">
    <p>Milan Rolie</p>
    <p>Based in Utrecht</p>
    <p>The Netherlands</p>
  </div> -->
</section>

<style>
  .hero-wrapper {
    position: relative;
    height: 85vh;
  }

  h1 {
    position: absolute;
    font-size: 9vw;
    line-height: 0.8em;
    font-weight: 400;
    top: 30%;
    left: 24%;
  }

  .inline-block {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
    /* background-color: aqua; */
  }

  .creative {
    margin-left: -20%;
  }

  .developer {
    /* clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%); */
  }

  .designer {
    /* clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%); */
  }

  .info-wrapper {
    position: absolute;
    bottom: 7%;
    left: 2.5%;
  }

  p {
    color: var(--flashWhite);
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 200;
  }

  .words {
    display: inline-block;
    /* transform: translateY( 200px); */
  }




</style>
