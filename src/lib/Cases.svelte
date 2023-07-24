<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    let caseClick = document.querySelector(".project");

    caseClick.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/about";
      }, 1000);
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

    gsap.to(".p1", {
      scrollTrigger: {
        trigger: ".p1",
        scrub: 2,
        start: "top-=1200",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      '--progress': 1
    });

    gsap.to(".p2", {
      scrollTrigger: {
        trigger: ".p2",
        scrub: 2,
        start: "top-=1200",
        end: "top-=200",
        stagger: 1,
        // markers: true,
      },
      y: 0,
      '--progress': 1
    });

    gsap.to(".p3", {
      scrollTrigger: {
        trigger: ".p3",
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

<div class="page-wrapper">
  <section class="projects-intro">
    <div class="line" />
    <h3 class="projects-text-gsap">projects</h3>
    <a class="view-all" href="">View all</a>
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
          <a class="subscript" href="">A better planet</a>
          <a class="subscript" href="">2022</a>
        </div>
        <a target="_blank" href="/about">
          <p class="view-project">
            Ink One page - Ink One page - Ink One page - Ink One page - Ink One
            page
          </p>

          <img
            src="https://images.unsplash.com/photo-1553877522-43269d4ea984?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80"
            alt="test"
          />
        </a>
      </div>
      <div class="project p2">
           <div class="subscripts">
          <a class="subscript" href="">A better planet</a>
          <a class="subscript" href="">2022</a>
        </div>
        <p class="view-project orange">
          50k for a better planet - 50k for a better planet - 50k for a better
          planet - 50k for a better planet - 50k for a better planet
        </p>
        <svg
          class="svg1"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          ><path
            d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
          /></svg
        >
        <p class="project-number">01</p>
        <img
          src="https://images.unsplash.com/photo-1493857671505-72967e2e2760?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80"
          alt="test"
        />
      </div>
      <div class="project p3">
        <div class="subscripts">
          <a class="subscript" href="">A better planet</a>
          <a class="subscript" href="">2022</a>
        </div>
        <a href="https://milanrolie.github.io/markk/" target="_blank">
          <p class="view-project orange">
            Markk - Markk - Markk - Markk - Markk - Markk - Markk - Markk
          </p>
          <svg
            class="svg1"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            ><path
              d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
            /></svg
          >
          <p class="project-number">01</p>
          <img
            src="https://images.unsplash.com/photo-1497215728101-856f4ea42174?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80"
            alt="test"
          />
        </a>
      </div>

      <!-- <div class="project">
        <a href="https://tiny-pink-monkey-cuff.cyclic.app/" target="_blank">
          <p class="view-project orange">
            UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV
            Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard -
            UltiTV Dashboard
          </p>
          <svg
            class="svg1"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            ><path
              d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
            /></svg
          >
          <p class="project-number">01</p>
          <img src="src/assets/dashboard.jpg" alt="test" />
        </a>
      </div>
      <div class="project">
        <a href="https://ubicautrecht.nl/" target="_blank">
          <p class="view-project black">
            Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica -
            Ubica
          </p>
          <svg
            class="svg1"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            ><path
              d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
            /></svg
          >
          <p class="project-number">01</p>
          <img
            src="https://twintig-utrecht.nl/wp-content/uploads/2022/01/Ubica-NSlagmolen-29-september-202119-scaled.jpg"
            alt="test"
          />
        </a>
      </div>
      <div class="project">
        <a href="https://family-fitness.nl/" target="_blank">
          <p class="view-project orange">
            Family Fitness - Family Fitness - Family Fitness - Family Fitness -
            Family Fitness - Family Fitness - Family Fitness
          </p>
          <svg
            class="svg1"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            ><path
              d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
            /></svg
          >
          <p class="project-number">01</p>
          <img
            src="https://images.unsplash.com/photo-1593476123561-9516f2097158?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80"
            alt="test"
          />
        </a>
      </div> -->
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
    font-size: .9em;
    padding: 0.4em 1em;
    border-radius: 1em;
    text-decoration: none;
    color: var(--gunMetal);
    text-transform: uppercase;
    transform: translateY(-5%);
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
    width: 100%;
    height: 70vh;
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0  round 1em);
    position: relative;
    overflow: hidden;
    margin-bottom: 2%;
  }

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

  .black {
    color: var(--dark);
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
  }

   img:hover {
    /* transform: scale(1.06); */
    /* filter: grayscale(1); */
  }

  .project:hover .view-project {
    opacity: 1;
  }

  .svg1 {
    display: none;
  }

  .project-number {
    display: none;
  }

  @media screen and (max-width: 1122px) {
    .projects-intro {
      margin-left: 0%;
    }

    h3 {
      font-size: 5em;
      color: var(--dark);
      font-weight: 300;
      line-height: 1em;
      text-transform: uppercase;
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
      width: 48%;
    }

    .text-wrapper {
      width: 0;
    }

    img {
      aspect-ratio: 0.7;
      width: 100%;
    }

    .project:hover img {
      transform: scale(1);
    }

    .svg1 {
      position: absolute;
      bottom: 3%;
      right: 3%;
      display: block;
      z-index: 2;
      fill: var(--webLavender);
    }

    .project-number {
      position: absolute;
      top: 3%;
      left: 3%;
      display: block;
      z-index: 2;
      color: var(--webLavender);
      font-size: 1.5em;
      font-weight: 300;
    }
  }

  @media screen and (max-width: 700px) {
    h3 {
      font-size: 3em;
      color: var(--dark);
      font-weight: 300;
      line-height: 1em;
      text-transform: uppercase;
    }

    .line {
      display: block;
      border: solid 1px var(--dark);
      margin: 2em 0;
      opacity: 0.5;
    }

    p {
      font-size: 1em;
    }

    .project {
      width: 100%;
    }

    .view-project {
      opacity: 1;
    }
  }
</style>
