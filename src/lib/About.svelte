<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.from(".about", {
      scrollTrigger: {
        trigger: ".image-wrapper",
        scrub: 1,
        start: "center-=300",
        end: "center",
        // markers: true,
      },
      y: 100,
    });

    gsap.from(".about-gsap", {
      scrollTrigger: {
        trigger: ".image-wrapper",
        scrub: 1,
        start: "center-=350",
        end: "center",
        // markers: true,
      },
      y: 100,
    });
  });
</script>

<section class="about">
  <!-- <div class="line"></div> -->
  <div class="text-wrapper">
    <!-- <h3>About</h3> -->
    <p class="about-gsap">
      As a creative individual, I am constantly seeking new ways to express my
      passion. Whether it's graphic design, photography, or web development.
    </p>
  </div>

  <!-- Currently, I am pursuing my studies in Amsterdam, where I further refine my
  skills and knowledge. I have had the privilege to learn from experienced
  professionals and work on challenging projects that have deepened my
  understanding of my field. Through my studies, I now combine the creative
  influences of my hometown with the academic and professional opportunities
  that Amsterdam has to offer.

I invite you to explore my portfolio and discover my work. Whether it's my designs, photographs, or other projects, I hope my passion and dedication shine through. If you're interested in my work or have a collaboration in mind, please don't hesitate to get in touch. I look forward to hearing from you! -->
</section>

<style>
  section {
    width: 100%;
    height: 70vh;
    padding: 0;
    background: linear-gradient(#0000 calc(100% - 2px), #0e0e0e);
    background-image: linear-gradient(#0000 calc(100% - 2px), #0e0e0e);
    background-position-y: 0.69vw;
    background-size: 1px 7vw;
    -webkit-clip-path: inset(1.4vw 0 0 0);
    clip-path: inset(1.4vw 0 0 0);
    font-size: 2.5vw;
    font-weight: 400;
    line-height: 7vw;
    position: relative;
    vertical-align: top;
    width: 100%;
    margin-bottom: 1vh;
    padding-left: 2%;
  }

  .text-wrapper {
    display: flex;
    flex-direction: row;
    /* margin-left: 10%; */
  }

  h3 {
    color: var(--flashWhite);
    font-weight: 300;
    font-size: 3em;
    margin-right: 5%;
  }

  p {
    font-size: 2.5em;
    font-weight: 200;
    /* max-width: 80%; */
  }

  p::selection {
    background: var(--bitterSweet);
  }

  @media screen and (max-width: 1122px) {
    p {
      font-size: 4.5em;
      /* text-transform: uppercase; */
      font-weight: 300;
      line-height: 1em;
      color: var(--flashWhite);
    }

    section {
      height: 21em;
      height: max-content;
      background: none;
      background-color: var(--dark);
      padding: 5em 1em ;
    }
  }

  @media screen and (max-width: 700px) {
    section {
      margin-top: 1%;
    }
  }
</style>
