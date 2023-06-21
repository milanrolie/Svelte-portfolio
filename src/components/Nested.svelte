<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".words", {
      y: 0,
      stagger: .3,
      delay: 1,
      duration: 1,
      ease: "power4.out",
    });

    gsap.to(".words", {
      scrollTrigger: {
        trigger: ".hero-wrapper",
        scrub: 1,
        start: "top",
        end: "top+=200",
        // markers: true,
      },
      x: -100,
      stagger: 0.5,
      duration: 1,
      ease: Power2.easeinOut,
    });

    gsap.to(".developer", {
      scrollTrigger: {
        trigger: ".hero-wrapper",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: 50,
      stagger: 0.5,
      duration: 1,
      ease: Power2.easeinOut,
    });

    gsap.to(".designer", {
      scrollTrigger: {
        trigger: ".hero-wrapper",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: -50,
      stagger: 0.5,
      duration: 1,
      ease: Power2.easeinOut,
    });

    gsap.to(".intro", {
      scrollTrigger: {
        trigger: ".hero-wrapper",
        scrub: 1,
        start: "top",
        end: "top+=200",
      },
      x: 150,
      stagger: 0.5,
      duration: 1,
      ease: Power2.easeinOut,
    });
  });
</script>

<section class="hero-wrapper">
  <h1>
    <div class="creative inline-block"><span class="words">creative</span></div>
    <div class="developer inline-block"><span class="words">developer &</span></div>
    <div class="designer inline-block"><span class="words">designer</span></div>
  </h1>
  <div class="info-wrapper">
    <p>Milan Rolie</p>
    <p>Based in Utrecht</p>
    <p>The Netherlands</p>
  </div>
</section>

<style>
  .hero-wrapper {
    position: relative;
    height: 85vh;
  }

  h1 {
    position: absolute;
    font-size: 9em;
    line-height: 0.8em;
    font-weight: 400;
    top: 30%;
    left: 24%;
  }

  .creative {
    margin-left: -20%;
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }

  .developer {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }

  .designer {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
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
    transform: translateY( 200px);
  }




</style>
