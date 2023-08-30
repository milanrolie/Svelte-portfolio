<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import grrr from "$lib/assets/grrr-iphone.webp";
  import favela from "$lib/assets/favela.webp";
  import markk from "$lib/assets/markk.webp";
  import ubica from "$lib/assets/ubicaMac.jpg";


  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    const goToPage = (url) => {
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(() => {
        window.location.href = url;
      }, 1000);
    };


    const viewAll = document.querySelector(".view-all");
    const caseClick1 = document.querySelector(".p1");
    const caseClick2 = document.querySelector(".p2");
    const caseClick3 = document.querySelector(".p3");
    const caseClick4 = document.querySelector(".p4");


    viewAll.addEventListener("click", (e) => {
      e.preventDefault();
      goToPage("/projects");
    });

    caseClick1.addEventListener("click", (e) => {
      e.preventDefault();
      goToPage("/a-better-planet");
    });

    caseClick2.addEventListener("click", (e) => {
      e.preventDefault();
      goToPage("/ink");
    });

    caseClick3.addEventListener("click", (e) => {
      e.preventDefault();
      goToPage("/markk");
    });

    caseClick4.addEventListener("click", (e) => {
      e.preventDefault();
      goToPage("/ubica");
    });

    gsap.to(".projects-text-gsap", {
      scrollTrigger: {
        trigger: ".page-wrapper",
        scrub: 2,
        start: "top-=800",
        end: "top-=300",
        // markers: true,
      },
      y: 0,
      rotate: 0,
    });

    const projects = [".p1", ".p2", ".p3", ".p4", ".p5,"];
    projects.forEach((project) => {
      gsap.to(project, {
        scrollTrigger: {
          trigger: project,
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
  });
</script>

<div class="page-wrapper">
  <section class="projects-intro">
    <div class="line" />
    <h3 class="projects-text-gsap">projects</h3>
    <a class="view-all" href="/projects">View all</a>
    <!-- <p>
      My projects are a mixture between real clients, personal and educational
      websites I've built.
    </p> -->
  </section>
  <div class="line2" />

  <section class="projects">
    <div class="projects-wrapper">
      <div class="project p1">
        <div class="subscripts">
          <div class="subscript">A better planet</div>
          <div class="subscript">2022</div>
        </div>
        <a href="https://studiorolie.com/a-better-planet">
          <p class="view-project js-view">
            50k for a better planet © 50k for a better planet © 50k for a better
            planet © 50k for a better planet © 50k for a better planet
          </p>
          <img src={grrr} alt="GRRR one page" />
        </a>
      </div>
      <div class="project p2">
        <div class="subscripts">
          <div class="subscript">A better planet</div>
          <div class="subscript">2022</div>
        </div>
        <a href="https://studiorolie.com/ink">
        <p class="view-project orange js-view2">
          Ink One page © Ink One page © Ink One page © Ink One page © Ink One
          page
        </p>
        <img src={favela} alt="Legends website" />
      </a>
      </div>
      <div class="project p3">
        <div class="subscripts">
          <div class="subscript">A better planet</div>
          <div class="subscript">2022</div>
        </div>
        <a href="https://studiorolie.com/markk">
          <p class="view-project blue">
            Markk © Markk © Markk © Markk © Markk © Markk © Markk © Markk
          </p>
          <img src={markk} alt="Markk Agency" />
        </a>
      </div>

      <div class="project p4">
        <div class="subscripts">
          <div class="subscript">Ubica Utrecht</div>
          <div class="subscript">2022</div>
        </div>
        <a href="https://studiorolie.com/ubica">
          <p class="view-project">
            Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica Utrecht
          </p>
          <img src={ubica} alt="Ubica Utrecht" />
        </a>
      </div>

      <div class="project p5">
        <div class="subscripts">
          <div class="subscript">Challem</div>
          <div class="subscript">2023</div>
        </div>
        <a href="https://studiorolie.com/markk">
          <p class="view-project blue">
            Challem © Challem © Challem © Challem © Challem © Challem © Challem © Challem
          </p>
          <img src={markk} alt="Markk Agency" />
        </a>
      </div>
    </div>
  </section>
</div>

<style>
  .projects-intro {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
    justify-content: space-between;
    margin-bottom: 2%;
    margin-top: 4%;
    clip-path: polygon(0 0, 220% 0, 220% 100%, 0% 100%);
  }

  .line {
    display: none;
  }

  h3 {
    font-size: 10vw;
    color: var(--dark);
    font-weight: 600;
    transform: translateY(100%) rotate(10deg);
  }

  .view-all {
    background-color: var(--dark);
    font-size: 0.9em;
    padding: 0.4em 1em;
    border-radius: 1em;
    text-decoration: none;
    color: var(--gunMetal);
    text-transform: uppercase;
    transform: translateY(-5%);
    transition: .2s;
  }

  .view-all:hover {
    background-color: var(--webLavender);
  }

  p {
    font-size: 1.5em;
    font-weight: 200;
    max-width: 40%;
    margin-left: 10%;
    margin-top: 2%;
    margin-bottom: 5%;
  }

  .line2 {
    margin: 2%;
    border-bottom: px solid var(--dark);
  }

  .projects {
    display: flex;
    flex-direction: row;
    height: max-content;
  }

  .projects-wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    gap: 2%;
    flex-wrap: wrap;
  }

  .project {
    position: relative;
    width: 100%;
    height: 70vh;
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0 round 1em);
    position: relative;
    overflow: hidden;
    margin-bottom: 2%;
  }

  /* .p2 {
    position: absolute;
  }
   */
  /* .active {
    width: 100vw;
    height: 100vh;
    z-index: 10;
  } */

  .view-project {
    display: flex;
    position: absolute;
    align-items: center;
    font-size: 10vw;
    z-index: 2;
    min-width: max-content;
    text-transform: uppercase;
    color: var(--webLavender);
    animation: projectMarquee 40s infinite linear;
    opacity: 0;
    height: 100%;
    width: max-content;
    transition: 0.2s;
    cursor: pointer;
    font-weight: 400;
    white-space: nowrap;
  }

  .orange {
    color: var(--bitterSweet);
  }

  /* .black {
    color: var(--dark);
  } */

  .blue {
    color: #6866fa;
  }

  .subscripts {
    position: absolute;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 5px;
    bottom: 4%;
    left: 2%;
    width: 95%;
  }

  .subscript {
    background-color: var(--dark);
    padding: 0.4em 1em;
    border-radius: 1em;
    text-decoration: none;
    color: var(--gunMetal);
    text-transform: uppercase;
  }

  @keyframes projectMarquee {
    0% {
      transform: translateX(0%);
    }

    100% {
      transform: translateX(-50%);
    }
  }

  img {
    /* aspect-ratio: 0.8; */
    object-fit: cover;
    border-radius: 1em;
    transition: 0.3s;
    cursor: pointer;
    z-index: 1;
    width: 100%;
    height: auto;
  }

  .project:hover .view-project {
    opacity: 1;
  }

  @media screen and (max-width: 1122px) {
    .projects-intro {
      margin-left: 0%;
    }

    h3 {
      font-size: 15vw;
      color: var(--dark);
    }

    p {
      font-size: 1.5em;
      font-weight: 200;
      max-width: 100%;
    }

    .projects-wrapper {
      width: 100%;
    }

    .project {
      width: 100%;
    }

    img {
      aspect-ratio: 0.7;
      width: 100%;
    }

    .view-project {
      opacity: 1;
    }
  }

  @media screen and (max-width: 700px) {
    h3 {
      font-size: 19vw;
    }

    p {
      font-size: 1em;
    }

    .project {
      width: 100%;
      height: 70svh;
    }

    .subscripts {
      position: absolute;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      gap: 5px;
      bottom: 1em;
      left: 2%;
      width: 95%;
    }

    .view-project {
      opacity: 1;
    }
  }
</style>
