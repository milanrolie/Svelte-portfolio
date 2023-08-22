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
  import challemIpad from "$lib/assets/challem-ipad.jpg"
  import challemMobile from "$lib/assets/challem-mobile.jpg"
  import bladmuziek from "$lib/assets/bladmuziek.jpg"
  import video from "$lib/assets/challem-video.mp4"



  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".words", {
      y: 0,
      delay: .8,
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
      '--progress': 1
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
      '--progress': 1
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
      '--progress': 1
    });

  });
</script>


<TransitionOut />
<Menu />
<Nav />

<section class="project-intro">
  <div class="text-wrapper">
    <h1 class="words">Challem</h1>
  </div>
  <div class="image">
    <!-- <p class="date">23-10-2020</p> -->
    <div class="img-clip">
    <img
      class="first-project-image"
      src={challemIpad}
      alt=" "
    />
  </div>
  </div>
  <div class="project-description">
    <div class="introduction">
      <p>
        Flowers are nature's delicate gems, adorning the world with their
        vibrant hues and captivating fragrances. They possess a unique ability
        to convey emotions, symbolizing love, gratitude, or sorrow. From the
        elegant roses to the cheerful sunflowers, each blossom tells a story,
        captivating our senses and uplifting our spirits.
      </p>
      <p>
        Beyond their aesthetic appeal, flowers play an essential role in
        ecosystems, attracting pollinators and supporting biodiversity. They
        bring life to gardens, parks, and landscapes, creating breathtaking
        displays of color.
      </p>
    </div>
    <div class="images">
      <img
        class="second-project-image project-clip-gsap "
        src={challemMobile}
        alt=""
      />
      <img
        class="second-project-image project-clip-gsap second-part2"
        src={bladmuziek}
        alt=""
      />
    </div>
    <div class="introduction">
      <p>
        Flowers are nature's delicate gems, adorning the world with their
        vibrant hues and captivating fragrances. They possess a unique ability
        to convey emotions, symbolizing love, gratitude, or sorrow. From the
        elegant roses to the cheerful sunflowers, each blossom tells a story,
        captivating our senses and uplifting our spirits.
      </p>
      <p>
        Beyond their aesthetic appeal, flowers play an essential role in
        ecosystems, attracting pollinators and supporting biodiversity. They
        bring life to gardens, parks, and landscapes, creating breathtaking
        displays of color.
      </p>
    </div>
    <div class="images">
      <video loop autoplay class="third-project-image project-clip-gsap" src={video}></video>
    </div>
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
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0  round 1em);
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
    width: 100%;
    height: 75vh;
    margin-bottom: 10%;
  }
  
  video {
    object-fit: cover;
    z-index: 2;
    border-radius: 1em;
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

    .date {
      font-size: .7em;
    }

    .introduction p {
      max-width: 100%;
      font-size: 1em;
    }


  }
</style>
