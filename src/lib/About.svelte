<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import arrow from "$lib/assets/arrow.svg";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.from(".about", {
      scrollTrigger: {
        trigger: ".about",
        scrub: 1,
        start: "top-=600",
        end: "top-=100",
        // markers: true,
      },
      y: 100,
    });

    gsap.from(".about-gsap", {
      scrollTrigger: {
        trigger: ".about",
        scrub: 2,
        start: "top-=600",
        end: "top-=100",
        // markers: true,
      },
      y: 100,
    });

    gsap.from(".about-gsap-late", {
      scrollTrigger: {
        trigger: ".about",
        scrub: 2,
        start: "top-=500",
        end: "top-=100",
        // markers: true,
      },
      y: 150,
    });

    // gsap.to(".portrait", {
    //   scrollTrigger: {
    //     trigger: ".about",
    //     scrub: 2,
    //     start: "top-=300",
    //     end: "top",
    //     // markers: true,
    //   },
    //   y: 0,
    //   '--progress': 1
    // });

    gsap.to(".about-words", {
      scrollTrigger: {
        trigger: ".about",
        scrub: 2,
        start: "top-=600",
        end: "top-=100",
        // markers: true,
      },
      y: 0,
    });
  });
</script>

<section class="about" id="about">
  <div class="wrapper">
    <div class="text-wrapper">
      <div class="left-wrapper">
        <p class="about-gsap">
          I'm a creatice developer based in Utrecht, the Netherlands. I love to
          build websites that are creative, functional and fitting to my
          clients.
        </p>

        <!-- <h4>what i do</h4> -->
        <p class="about-gsap" />
      </div>
      <div class="right-wrapper">
        <h3>
          <div class="creative inline-block">
            <span class="about-words">Creative</span>
          </div>
          <div class="developer inline-block">
            <span class="about-words">Developer +</span>
          </div>
          <div class="designer inline-block">
            <span class="about-words">Designer</span>
          </div>
        </h3>
        <p class="about-gsap-late">
          I'm Milan, a freelance designer and developer located in Utrecht. My
          skill set covers a wide range of projects, including graphic design,
          WordPress and custom-coded websites, as well as photography. I
          embarked on this journey in 2018 and have been passionately pursuing
          it ever since. I look forward to the opportunity of collaborating with
          you to bring your creative visions to life.
        </p>
      </div>
      <img src={arrow} alt="Arrrow" />
    </div>
    <!-- <img class="portrait" src="https://images.unsplash.com/photo-1517101552363-df64abce174a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1103&q=80" alt=""> -->
  </div>
</section>

<style>
  section {
    width: 100%;
    height: 110vh;
    position: relative;
    width: 100%;
    padding: 0 2%;
    margin-top: 2%;
  }

  .wrapper {
    width: 100%;
    height: 100%;
    background-color: var(--dark);
    border-radius: 1em;
    padding: 1em;
    padding-bottom: 0;
  }

  .text-wrapper {
    display: flex;
    flex-direction: row;
    gap: 2em;
  }

  h3 {
    color: var(--gunMetal);
    font-weight: 300;
    font-size: 4.5vw;
    margin-right: 5%;
    line-height: 1em;
  }

  .developer {
    margin-left: 10%;
  }

  .designer {
    padding-bottom: 1%;
    margin-bottom: 2%;
  }

  .about-words {
    display: inline-block;
    transform: translateY(200px);
  }

  .inline-block {
    clip-path: polygon(0 0, 220% 0, 220% 100%, 0% 100%);
  }

  .left-wrapper p {
    font-size: 5vw;
    font-weight: 300;
    color: var(--gunMetal);
    line-height: 1em;
  }

  ::selection {
    background: var(--bitterSweet);
  }

  .left-wrapper {
    width: 100%;
    z-index: 2;
  }

  .right-wrapper {
    padding-left: 10%;
    width: 100%;
    margin-top: 10%;
  }

  .right-wrapper p {
    font-size: 1.5em;
    color: var(--gunMetal);
    max-width: 60%;
    font-weight: 200;
    line-height: 1em;
  }

  img {
    position: absolute;
    aspect-ratio: 1;
    left: 0em;
    bottom: 0em;
    width: 10vw;
    /* height: 30vh; */
    object-fit: cover;
    z-index: 1;
    /* opacity: .5; */
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0 round 1em);
    transform: translateY(0px);
  }

  @media screen and (max-width: 1122px) {
    p {
      font-size: 4.5em;
      font-weight: 300;
      line-height: 1em;
      color: var(--flashWhite);
    }

    section {
      height: 100vh;
      background: none;
    }

    .right-wrapper p {
      font-size: 1.1em;
      max-width: 90%;
    }

    img {
      left: 1em;
      bottom: 1em;
      width: 10vw;
      /* height: 30vh; */
    }
  }

  @media screen and (max-width: 700px) {
    section {
      margin-top: 1%;
      height: max-content;
    }

    .text-wrapper {
      display: flex;
      flex-direction: column;
      gap: 3em;
    }

    .left-wrapper p {
      font-size: 10vw;
    }

    .right-wrapper p {
      font-size: 1.1em;
      max-width: 100%;
      margin-bottom: 20%;
    }

    h3 {
      font-size: 10vw;
    }

    .right-wrapper {
      padding-left: 25%;
    }
  }
</style>
