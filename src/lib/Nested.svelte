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
      y: 400,
      // stagger: .3,
      delay: 4,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.to(".image-wrapper", {
      y: 0,
      // stagger: .3,
      delay: 4.5,
      duration: 1.5,
      ease: "power4.out",
    });


    gsap.to(".showreel", {
      scrollTrigger: {
        trigger: ".image-wrapper",
        scrub: 1,
        start: "top-=800",
        end: "top+=200",
        // markers: true,
      },
      y: -50,
    });
  });
</script>

<section class="hero-wrapper">
  <div class="text-wrapper">
  <h1>
    <div class="creative inline-block"><span class="words">Studio</span></div>
    <div class="developer inline-block">
      <span class="words">rolie</span>
    </div>
    <!-- <div class="designer inline-block"><span class="words">Designer</span></div> -->
  </h1>
  <!-- <div class="info-wrapper">
    <p>Milan Rolie</p>
    <p>Based in Utrecht</p>
    <p>The Netherlands</p>
  </div> -->
</div>
<div class="image-wrapper">
  <!-- <div class="showreel-overlay"></div> -->
  <img class="showreel" src="https://images.unsplash.com/photo-1527148191484-193c02d12e83?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="">
</div>
</section>

<style>
  .hero-wrapper {
    position: relative;
    overflow: hidden;
  }

  .text-wrapper {
    height: 65vh;
  }

  h1 {
    position: absolute;
    font-size: 25.5vw;
    line-height: 0.8em;
    font-weight: 700;
    top: 1%;
    left: 0;
    text-transform: lowercase;
  }

  .inline-block {
    clip-path: polygon(0 0, 220% 0, 220% 100%, 0% 100%);
  }

  .developer {
    margin-left: 65.3%;
    transform: translateY(-30%);
  }

  .words {
    display: inline-block;
    /* transform: translateY( 200px); */
  }

  .image-wrapper {
    height: 80vh;
    position: relative;
    overflow: hidden;
    transform: translateY(50%);
    border-radius: 1em;
  }

  /* .showreel-overlay {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: black;
    opacity: 0.1;
    z-index: 3;
    transition: .5s;
    border-radius: 1em;
  } */

  img {
    width: 100%;
    height: 130%;
    object-fit: cover;
  }

  @media screen and (max-width: 1122px) {
    .hero-wrapper {
      height: max-content;
    }

    .text-wrapper {
    height: 50vh;
  }

    h1 {
      font-size: 25vw;
      position: relative;
      line-height: 1em;
      font-weight: 600;
      left: 0;
    }

    .creative {
    margin-left: 0;
  }

  .developer {
    margin-left: 47%;
  }  
  }

  @media screen and (max-width: 700px) {
    h1 {
      font-size: 26vw;
      padding-top: 13%;
    }

    .developer {
    margin-left: 48.5%;
  }  

  .text-wrapper {
    height: 38svh;
  }

  .image-wrapper {
    height: 80svh;
    position: relative;
    overflow: hidden;
    transform: translateY(300px);
    border-radius: 1em;
  }
  }
</style>
