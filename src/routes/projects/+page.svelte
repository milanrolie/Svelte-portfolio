<script>
  import Nav from "$lib/Nav.svelte";
  import OtherProjects from "$lib/OtherProjects.svelte";
  import Footer from "$lib/Footer.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import grrr from "$lib/assets/grrr-iphone.webp";
  import legends from "$lib/assets/legends-macbook2.webp";
  import favela from "$lib/assets/favela.webp";
  import markk from "$lib/assets/markk.webp";
  import arrow from "$lib/assets/arrow.svg";
  import highTea from "$lib/assets/high-tea-low.jpg";
  import commentary from "$lib/assets/commentary-tool.jpg";
  import fitness from "$lib/assets/fitness.jpg";
  import challem from "$lib/assets/challem.jpg";
  import squad from "$lib/assets/squad.jpg";
  import twintig from "$lib/assets/twintig.jpg";
  import Lenis from "@studio-freight/lenis";
  import Menu from "../../lib/Menu.svelte";
  import TransitionOut from "../../lib/TransitionOut.svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    let p1 = document.querySelector(".p1");
    let p2 = document.querySelector(".p2");
    let p3 = document.querySelector(".p3");
    let p4 = document.querySelector(".p4");
    let p5 = document.querySelector(".p5");
    let p6 = document.querySelector(".p6");
    let p7 = document.querySelector(".p7");
    let p8 = document.querySelector(".p8");
    let p9 = document.querySelector(".p9");
    let p10 = document.querySelector(".p10");

    const lenis = new Lenis({
      duration: 1.5,
      easing: (t) => (t === 1 ? 1 : 1 - Math.pow(2, -10 * t)),
      orientation: "horizontal",
      gestureOrientation: "vertical",
      orientation: "horizontal",
      smoothWheel: true,
      smoothTouch: false,
      touchMultiplier: 2,
    });

    function raf(time) {
      lenis.raf(time);
      requestAnimationFrame(raf);
    }

    requestAnimationFrame(raf);

    lenis.on("scroll", () => {
    });

    function raf(time) {
      lenis.raf(time);
      requestAnimationFrame(raf);
    }

    requestAnimationFrame(raf);

    lenis.on("scroll", ScrollTrigger.update);

    gsap.ticker.add((time) => {
      lenis.raf(time * 1000);
    });

    gsap.ticker.lagSmoothing(0);

    let mm = gsap.matchMedia();
    mm.add("(min-width: 701px)", () => {
      gsap.from(".case", {
        duration: 1,
        delay: 0.5,
        stagger: 0.3,
        y: "150%",
      });
    });

    mm.add("(max-width: 700px)", () => {
      gsap.to(".projects", {
      y: 0,
      delay: .8,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.from(".projects-wrapper", {
      y: 500,
      delay: 1,
      duration: 1.5,
      ease: "power4.out",
    });
    
    });

    p1.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/a-better-planet";
      }, 1000);
    });

    p2.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/ink";
      }, 1000);
    });

    p3.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/markk";
      }, 1000);
    });

    p4.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/twintig";
      }, 1000);
    });

    p5.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/commentary-tool";
      }, 1000);
    });

    p6.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/ubica";
      }, 1000);
    });

    p7.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/squad-page";
      }, 1000);
    });

    p8.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/family-fitness";
      }, 1000);
    });

    p9.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "/challem";
      }, 1000);
    });

    p10.addEventListener("click", function (e) {
      e.preventDefault();
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(function () {
        window.location.href = "https://studiorolie.com/#contact";
      }, 1000);
    });
  });
</script>

<TransitionOut />
<Nav />
<Menu />

<section class="cases">
  <h1 class="projects">projects</h1>
  <div class="projects-wrapper">
    <div class="case p1">
      <div class="subscripts">
        <div class="subscript" href="">A better planet</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/a-better-planet">
        <p class="view-project js-view">
          50k for a better planet © 50k for a better planet © 50k for a better
          planet © 50k for a better planet © 50k for a better planet
        </p>

        <img src={grrr} alt="GRRR one page" />
      </a>
    </div>

    <div class="case p2 high">
      <div class="subscripts">
        <div class="subscript" href="">Ink football</div>
        <div class="subscript" href="">2023</div>
      </div>
      <a href="/ink">
        <p class="view-project js-view orange">
          Ink football © Ink football © ink football planet © Ink football © Ink
          football
        </p>

        <img src={favela} alt="Ink Football" />
      </a>
    </div>
    <div class="case p3">
      <div class="subscripts">
        <div class="subscript" href="">Markk Agency</div>
        <div class="subscript" href="">2023</div>
      </div>
      <a href="/markk">
        <p class="view-project js-view blue">
          Markk © Markk © Markk © Markk © Markk © Markk © Markk © Markk © Markk
        </p>
        <img src={markk} alt="Markk Agency" />
      </a>
    </div>
    <!-- <div class="case p4 high">
      <div class="subscripts">
        <div class="subscript" href="">Twintig Utrecht</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/twintig">
        <p class="view-project js-view">
          Twintig Utrecht © Twintig Utrecht © Twintig Utrecht © Twintig Utrecht
          © Twintig Utrecht
        </p>
        <img src={twintig} alt="Twintig Utrecht" />
      </a>
    </div>
    <div class="case p5">
      <div class="subscripts">
        <div class="subscript" href="">Commentary tool</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/commentary-tool">
        <p class="view-project js-view orange">
          Commentary tool © Commentary tool © Commentary tool © Commentary tool
          © Commentary tool
        </p>
        <img src={commentary} alt="Commentary tool" />
      </a>
    </div> -->
    <div class="case p6 high">
      <div class="subscripts">
        <div class="subscript" href="">Ubica Utrecht</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/ubica">
        <p class="view-project js-view">
          Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica Utrecht © Ubica
          Utrecht
        </p>
        <img src={highTea} alt="Ubica Utrecht" />
      </a>
    </div>
    <div class="case p7">
      <div class="subscripts">
        <div class="subscript" href="">FDND squad page</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/squad-page">
        <p class="view-project js-view">
          FDND squad page © FDND squad page © FDND squad page © FDND squad page
          © FDND squad page
        </p>
        <img src={squad} alt="FDND squad page" />
      </a>
    </div>
    <div class="case p8 high">
      <div class="subscripts">
        <div class="subscript" href="">Family Fitness</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/family-fitness">
        <p class="view-project js-view">
          Family Fitness © Family Fitness © Family Fitness © Family Fitness ©
          Family Fitness
        </p>
        <img src={fitness} alt="Family Fitness" />
      </a>
    </div>
    <div class="case p9">
      <div class="subscripts">
        <div class="subscript" href="">Challem</div>
        <div class="subscript" href="">2022</div>
      </div>
      <a href="/challem">
        <p class="view-project js-view">
          Challem © Challem © Challem © Challem © Challem © Challem © Challem
        </p>
        <img src={challem} alt="Challem" />
      </a>
    </div>
    <div class="case p10 high">
      <div class="subscripts show">
        <div class="subscript show" href="">Your project here?</div>
        <div class="subscript show" href="">anytime</div>
      </div>
      <a href="https://studiorolie.com#contact">
        <p class="view-project js-view view-content show">
          Your project here? © Your project here? © Your project here? © Your
          project here? © Your project here?
        </p>
        <!-- <img src={favela} alt="Your project here?" /> -->
      </a>
    </div>
  </div>

  <footer>
    <p>studio rolie</p>
    <p />
    <img src={arrow} alt="" />
    <div class="progress-bar">
      <div class="bar" />
    </div>
  </footer>
</section>

<style>
  .cases {
    height: 100vh;
    width: max-content;
    padding: 5% 2% 5% 2%;
    width: max-content;
    overflow-y: hidden;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    /* background-color: var(--dark); */
  }

  h1 {
    position: fixed;
    top: 2.5%;
    left: 10%;
    font-weight: 600;
    font-size: 2vh;
    margin-bottom: 2%;
  }

  .projects {
    transform: translateY(700px);
  }

  .projects-wrapper {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
    gap: 2em;
  }

  .case {
    position: relative;
    width: 75vh;
    height: 50vh;
    overflow: hidden;
    clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0 round 1em);
  }

  .view-project {
    display: flex;
    position: absolute;
    align-items: flex-end;
    font-size: 9vw;
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
    padding-bottom: 20vh;
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
    bottom: .9em;
    left: 2%;
    width: 95%;
    opacity: 0;
    transition: 0.3s;
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

  .case img {
    width: 100%;
    height: 100%;
    transition: 0.5s;
    object-fit: cover;
    border-radius: 1em;
  }

  .high {
    height: 80vh;
    width: 65vh;
  }

  a {
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .case:hover .view-project {
    opacity: 1;
  }

  .case:hover .subscripts {
    opacity: 1;
  }

  .show {
    opacity: 1;
  }

  .show div {
    background-color: var(--gunMetal);
    color: var(--dark);
  }

  .p10 {
    background-color: var(--dark);
    border-radius: 1em;
  } 
  footer {
    position: fixed;
    left: 0;
    bottom: 0;
    display: flex;
    align-items: center;
    width: 100vw;
    height: 5vh;
    padding: 0 2%;
  }

  /* footer img {
    position: absolute;
    right: 2%;
    transform: rotate(270deg);
  } */

  .progress-bar {
    position: absolute;
    right: 1.5%;
    width: 10em;
    height: 4px;
    background-color: rgb(154, 154, 154);
    border-radius: 1em;
    overflow: hidden;
  }

  .bar {
    height: 100%;
    width: 100%;
    background-color: var(--dark);
    transform: translateX(-100%);
  }

  @media screen and (max-width: 1122px) {
    .view-project {
      opacity: 1;
    }

    .subscripts {
      opacity: 1;
    }
  }

  @media screen and (max-width: 700px) {
    .cases {
      height: auto;
      padding: 40% 2% 2% 2%;
      width: max-content;
      overflow-y: visible;
      overflow-x: hidden;
    }

    h1 {
    position: relative;
    top: 2.5%;
    left: 1%;
    font-weight: 600;
    font-size: 10vh;
    margin-bottom: 5%;
  }

    .projects-wrapper {
      flex-direction: column;
    }

    .case {
      position: relative;
      width: 100vw;
      height: 80vh;
      overflow: hidden;
      clip-path: inset(calc((1 - var(--progress)) * 100%) 0 0 0 round 1em);
    }

    .view-project {
      font-size: 20vw;
      justify-content: center;
      align-items: center;
      padding-bottom: 0;
    }

    footer {
      display: none;
    }

    

    
  }
</style>
