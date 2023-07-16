<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".words", {
      scrollTrigger: {
        trigger: ".hero-wrapper",
        scrub: 1,
        start: "top+=20",
        end: "center+=200",
      },
      y: -150,

    });

    gsap.from(".words", {
      y: 200,
      // stagger: .3,
      delay: 4,
      duration: 1.5,
      ease: "power4.out",
    });
  });
</script>

<section class="hero-wrapper">
  <h1>
    <div class="creative inline-block"><span class="words">Creative</span></div>
    <div class="developer inline-block">
      <span class="words">Developer +</span>
    </div>
    <div class="designer inline-block"><span class="words">Designer</span></div>
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

  @media screen and (max-width: 1122px) {
    .hero-wrapper {
      height: 40vh;
    }

    h1 {
      font-size: 13vw;
      position: relative;
      line-height: 1em;
      font-weight: 400;
      left: 0;
    }

    .creative {
    margin-left: 0;
  }

  .developer {
    /* clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%); */
  }

  .designer {
    /* clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%); */
  }
  }

  @media screen and (max-width: 700px) {
    h1 {
      font-size: 13vw;
    }
  }
</style>
