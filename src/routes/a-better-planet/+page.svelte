<script>
  import Nav from "$lib/Nav.svelte";
  import Transition from "$lib/Transition.svelte";
  import OtherProjects from "$lib/OtherProjects.svelte";
  import Footer from "$lib/Footer.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import TransitionOut from "../../lib/TransitionOut.svelte";
  import AllProjects from "../../lib/allProjects.svelte";
  import Menu from "../../lib/Menu.svelte";
  import headImage from "$lib/assets/ABPlanet-mac.jpg";
  import video from "$lib/assets/aBetterPlanet_lowRes.mp4";
  import grrr from "$lib/assets/grrr-iphone.webp";



  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".words", {
      y: 0,
      delay: 0.8,
      duration: 1.5,
      ease: "power4.out",
    });

    // gsap.to(".words", {
    //   scrollTrigger: {
    //     trigger: ".text-wrapper",
    //     scrub: 1,
    //     start: "top",
    //     end: "center",
    //     markers: true,
    //   },
    //   y: 0,
    // });

    gsap.to(".first-project-image", {
      scrollTrigger: {
        trigger: ".image",
        scrub: 1,
        start: "top-=200",
        end: "center+=200",
        // markers: true,
      },
      scale: 1.07,
    });

    gsap.from(".first-project-image", {
      y: 500,
      delay: 1,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.from(".date", {
      y: 500,
      delay: 1.7,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.to(".second-project-image", {
      scrollTrigger: {
        trigger: ".second-project-image",
        scrub: 2,
        start: "top-=1200",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      "--progress": 1,
    });

    gsap.to(".second-part2", {
      scrollTrigger: {
        trigger: ".second-part2",
        scrub: 2,
        start: "top-=1000",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      "--progress": 1,
    });

    gsap.to(".third-project-image", {
      scrollTrigger: {
        trigger: ".third-project-image",
        scrub: 2,
        start: "top-=1200",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      "--progress": 1,
    });
  });
</script>

<TransitionOut />
<Menu />
<Nav />

<section class="project-intro">
  <div class="text-wrapper">
    <h1 class="words">A better planet</h1>
    <!-- <p class="date">23-10-2020</p> -->
  </div>
  <div class="image">
    <div class="img-clip">
      <img
        class="first-project-image"
        src={headImage}
        alt=" "
      />
    </div>
  </div>
  <div class="project-description">
    <div class="introduction">
      <p>
        This is a project I have done as an school project in collaboration with
        Lama lama. Lama Lama is a creative digital agency. They deliver digital
        changes for companies with a conscience and brands with a heart. They
        embrace a fluid approach, and use our expertise to create longevity and
        value for our clients. Together with them they hope to make the world a
        little better.
      </p>
      <p>
        In this project I had to make a website for a company called Ink. Ink is
        an organisation who help children in Brazil to get them from the streets
        and educate them with the right tools and knowledge. The website is a
        landing page where visitors can see the progress Ink has made with
        helping children.
      </p>
    </div>
    <div class="images">
      <img
        class="second-project-image project-clip-gsap"
        src={grrr}
        alt=""
      />
      <img
        class="second-project-image project-clip-gsap second-part2"
        src="https://images.unsplash.com/photo-1591025207163-942350e47db2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjZ8fHN1c3RhaW5hYmlsaXR5fGVufDB8fDB8fHww&auto=format&fit=crop&w=500&q=60"
        alt=""
      />
    </div>
    <div class="introduction">
      <p>
      test
      </p>
      <p>
        Beyond their aesthetic appeal, flowers play an essential role in
        ecosystems, attracting pollinators and supporting biodiversity. They
        bring life to gardens, parks, and landscapes, creating breathtaking
        displays of color.
      </p>
    </div>
    <div class="images">
      <video loop autoplay in class="third-project-image project-clip-gsap" src={video}></video>

  </div>
</section>

<OtherProjects />
<Footer />

<style>
  section {
    /* padding: 0; */
    overflow-x: hidden;
  }

  .text-wrapper {
    position: sticky;
    top: 0;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    height: 60vh;
    padding: 2%;
    margin-bottom: 2%;
    z-index: -1;
  }

  h1 {
    color: var(--dark);
    font-size: 9vw;
    text-transform: none;
    line-height: 0.8em;
    font-weight: 600;
  }

  .words {
    transform: translateY(700px);
  }

  .date {
    position: absolute;
    right: 1%;
    top: -6%;
    font-weight: 400;
    padding: 0.5em 1em;
    border: solid 2px;
    border-radius: 2em;
    color: var(--gunMetal);
    background-color: var(--dark);
  }

  .img-clip {
    height: 100%;
    width: 100%;
    border-radius: 1em;
    overflow: hidden;
  }

  .project-clip-gsap {
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0 round 1em);
  }

  .image {
    position: relative;
    margin-bottom: -5px;
  }

  img {
    object-fit: cover;
    z-index: 2;
    border-radius: 1em;
  }

  video {
    object-fit: cover;
    z-index: 2;
    border-radius: 1em;
  }

  .first-project-image {
    width: 100%;
    height: 95vh;
  }

  .project-description {
    background-color: var(--gunMetal);
    padding-top: 7%;
  }

  .introduction {
    display: flex;
    flex-direction: row;
    gap: 5%;
    padding: 3% 20%;
    margin-bottom: 3%;
  }

  .introduction p {
    font-size: 1.2em;
    font-weight: 300;
    max-width: 40%;
  }

  .images {
    display: flex;
    flex-direction: row;
    gap: 2%;
    padding: 0% 20%;
    width: 100%;
  }

  .second-project-image {
    width: 50%;
    height: 75vh;
  }

  .third-project-image {
    width: 102%;
    height: 75vh;
    margin-bottom: 10%;
  }

  @media screen and (max-width: 1122px) {
    .text-wrapper {
      height: 30%;
      margin-top: 40%;
    }

    .introduction {
      flex-direction: column;
      padding: 5% 15%;
    }

    .introduction p {
      max-width: 90%;
      margin-bottom: 1em;
    }

    .images {
      display: flex;
      flex-direction: column;
      padding: 0% 10%;
    }

    .second-project-image {
      width: 100%;
      height: 50%;
      margin-bottom: 5%;
    }
  }

  @media screen and (max-width: 700px) {
    .first-project-image {
      width: 100%;
      height: 120%;
    }

    .images {
      padding: 0;
    }

    .date {
      font-size: 0.7em;
      display: none;
    }

    .introduction p {
      max-width: 100%;
      font-size: 1em;
    }
  }
</style>
