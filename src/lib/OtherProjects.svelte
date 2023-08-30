<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import arrow from "$lib/assets/arrow.svg";

  import grrr from "$lib/assets/grrr-iphone.jpg";
  import legends from "$lib/assets/legends-macbook2.jpg";
  import favela from "$lib/assets/favela.jpg";
  import markk from "$lib/assets/markk.jpg";
  import highTea from "$lib/assets/high-tea-low.jpg";
  import commentary from "$lib/assets/commentary-tool.jpg";
  import fitness from "$lib/assets/fitness.jpg";
  import challem from "$lib/assets/challem.jpg";
  import squad from "$lib/assets/squad.jpg";
  import twintig from "$lib/assets/twintig.jpg";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".others-gsap", {
      scrollTrigger: {
        trigger: ".clip",
        scrub: 2,
        start: "top-=600",
        end: "top-=100",
        // markers: true,
      },
      y: 0,
      rotate: 0,
    });

    gsap.to(".allProjects-gsap", {
      scrollTrigger: {
        trigger: ".clip",
        scrub: 1,
        start: "top-=600",
        end: "top-=100",
        // markers: true,
      },
      y: 0,
      rotate: 0,
    });

    gsap.to(".allRight-gsap", {
      x: 0,
      duration: 1,
      stagger: 0.4,
      scrollTrigger: {
        trigger: ".clip",
        scrub: 1,
        start: "top-=600",
        end: "top-=100",
        toggleActions: "play none none none",

        // markers: true,
      },
    });

    gsap.to(".tag", {
      x: 0,
      opacity: 1,
      duration: 1,
      stagger: 0.1,
      scrollTrigger: {
        trigger: ".clip",
        start: "top-=600",
        end: "top-=100",
        toggleActions: "play none none none",
        // markers: true,
      },
    });

    const hoverElement1 = document.querySelector(".first");
    const projectImage1 = document.querySelector(".project-image1");
    const hoverElement2 = document.querySelector(".second");
    const projectImage2 = document.querySelector(".project-image2");
    const hoverElement3 = document.querySelector(".third");
    const projectImage3 = document.querySelector(".project-image3");
    const hoverElement4 = document.querySelector(".fourth");
    const projectImage4 = document.querySelector(".project-image4");
    // const hoverElement5 = document.querySelector(".fifth");
    // const projectImage5 = document.querySelector(".project-image5");
    const hoverElement6 = document.querySelector(".sixt");
    const projectImage6 = document.querySelector(".project-image6");

    hoverElement1.addEventListener("mouseenter", () => {
      projectImage1.classList.toggle("view");
    });

    hoverElement1.addEventListener("mouseleave", () => {
      projectImage1.classList.toggle("view");
    });

    hoverElement2.addEventListener("mouseenter", () => {
      projectImage2.classList.toggle("view");
    });

    hoverElement2.addEventListener("mouseleave", () => {
      projectImage2.classList.toggle("view");
    });

    hoverElement3.addEventListener("mouseenter", () => {
      projectImage3.classList.toggle("view");
    });

    hoverElement3.addEventListener("mouseleave", () => {
      projectImage3.classList.toggle("view");
    });

    hoverElement4.addEventListener("mouseenter", () => {
      projectImage4.classList.toggle("view");
    });

    hoverElement4.addEventListener("mouseleave", () => {
      projectImage4.classList.toggle("view");
    });

    // hoverElement5.addEventListener("mouseenter", () => {
    //   projectImage5.classList.toggle("view");
    // });

    // hoverElement5.addEventListener("mouseleave", () => {
    //   projectImage5.classList.toggle("view");
    // });

    hoverElement6.addEventListener("mouseenter", () => {
      projectImage6.classList.toggle("view");
    });

    hoverElement6.addEventListener("mouseleave", () => {
      projectImage6.classList.toggle("view");
    });

    const links = [
      { class: ".p1", url: "/a-better-planet" },
      { class: ".p2", url: "/ink" },
      { class: ".p3", url: "/markk" },
      { class: ".p4", url: "/ubica" },
      // { class: ".p5", url: "/commentary-tool" },
      // { class: ".p5", url: "/family-fitness" },
      { class: ".p6", url: "/challem" },
      // { class: ".p8", url: "/twintig" },
      // { class: ".p9", url: "/squad-page" },
    ];

    links.forEach((link) => {
      const el = document.querySelector(link.class);
      el.addEventListener("click", function (e) {
        e.preventDefault();
        gsap.to(".transition", {
          y: "-10%",
          rotate: 0,
          delay: 0,
          stagger: 0,
          duration: 1,
        });
        setTimeout(function () {
          window.location.href = link.url;
        }, 1000);
      });
    });
  });
</script>

<section>
  <div class="wrapper">
    <div class="clip">
      <h3 class="others-gsap">others</h3>
    </div>
    <ul>
      <a class="p1" href="/a-better-planet">
        <li class="first">
          <div class="clip">
            <p class="allProjects-gsap">
              A better planet <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">Design</p>
            <p class="tag">Animations</p>
          </div>

          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a>
      <a class="p2" href="/ink">
        <li class="second">
          <div class="clip">
            <p class="allProjects-gsap">
              Ink football <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">Animations</p>
          </div>

          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a>
      <a class="p3" href="/markk">
        <li class="third">
          <div class="clip">
            <p class="allProjects-gsap">
              Markk agency <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">Design</p>
            <p class="tag">Animations</p>
          </div>

          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a>
      <a class="p4" href="/ubica">
        <li class="fourth">
          <div class="clip">
            <p class="allProjects-gsap">
              Grand café Ubica <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">Design</p>
          </div>

          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a>
      <!-- <a class="p5" href="/commentary-tool">
        <li class="second">
          <div class="clip">
            <p class="allProjects-gsap">
              Commentary tool <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">UX</p>
            <p class="tag">Data</p>
          </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a> -->
      <!-- <a class="p5" href="/family-fitness">
        <li class="fifth">
          <div class="clip">
            <p class="allProjects-gsap">
              Family fitness <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">video</p>
          </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a> -->
      <a class="p6" href="/challem">
        <li class="sixt">
          <div class="clip">
            <p class="allProjects-gsap">
              Challem <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
          </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a>
      <!-- <a class="p8" href="/twintig">
        <li class="fifth">
          <div class="clip">
            <p class="allProjects-gsap">
              Twintig Utrecht <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">design</p>
          </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a> -->
      <!-- <a class="p9" href="/squad-page">
        <li class="sixt">
          <div class="clip">
            <p class="allProjects-gsap">
              Fdnd squad profile page <img src={arrow} alt="" />
            </p>
          </div>
          <div class="tags">
            <p class="tag">Website</p>
            <p class="tag">design</p>
            <p class="tag">data</p>
          </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
        </li>
      </a> -->
    </ul>
    <div class="image-wrapper">
      <img class="project-image project-image" src={arrow} alt="" />

      <img class="project-image project-image1 view" src={grrr} alt="" />

      <img class="project-image project-image2 view" src={legends} alt="" />

      <img class="project-image project-image3 view" src={markk} alt="" />

      <img class="project-image project-image4 view" src={highTea} alt="" />

      <img class="project-image project-image5 view" src={fitness} alt="" />

      <img class="project-image project-image6 view" src={challem} alt="" />
      <div class="image-overlay" />
    </div>
  </div>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    position: relative;
    width: 100%;
    margin-bottom: 4%;
    height: max-content;
  }

  .wrapper {
    height: 100%;
    background-color: var(--dark);
    border-radius: 1em;
  }

  .clip {
    clip-path: polygon(0 0, 220% 0, 220% 100%, 0% 100%);
  }

  h3 {
    color: var(--gunMetal);
    font-size: 10vw;
    font-weight: 600;
    margin-left: 2%;
    line-height: 1;
    transform: translateY(100%) rotate(10deg);
  }

  ul {
    display: flex;
    flex-direction: column;
  }

  li {
    display: flex;
    position: relative;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    text-decoration: none;
    list-style: none;
    font-size: 3vw;
    padding: 1px;
    padding: 1% 2%;
    transition: 0.3s;
    overflow: hidden;
    text-transform: lowercase;
    font-weight: 200;
  }

  a {
    text-decoration: none;
  }

  p {
    position: relative;
    color: var(--gunMetal);
    /* transition: 0.3s; */
    display: flex;
    flex-direction: row;
  }

  .allProjects-gsap {
    transform: translateY(100%);
  }

  .tags {
    position: absolute;
    top: 30%;
    left: 45%;
    display: flex;
    flex-direction: row;
    gap: 0.4em;
  }

  .tag {
    background-color: none;
    font-size: 0.4em;
    padding: 0.3em 1em;
    border-radius: 1em;
    text-decoration: none;
    color: var(--gunMetal);
    text-transform: uppercase;
    border: solid 1px var(--gunMetal);
    transform: translateX(50px);
    opacity: 0;
  }

  li:hover {
    cursor: pointer;
  }

  ul .date2 {
    font-size: 0.5em;
    transform: translateX(200px);
  }

  li img {
    position: absolute;
    object-fit: cover;
    right: -0.8em;
    height: 2vw;
    width: 2vw;
    transform: translateY(55%);
    margin-left: 3%;
    opacity: 0;
    transition: 0.8s;
  }

  li:hover img {
    opacity: 1;
  }

  .image-wrapper {
    position: relative;
    width: 100%;
    height: 10em;
    overflow: hidden;
  }

  .project-image {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 0 0 1em 1em;
    z-index: 2;
    transition: 0.5s;
  }

  .project-image1 {
    opacity: 1;
  }

  .view {
    opacity: 0;
  }

  .image-overlay {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: var(--dark);
    opacity: 0.2;
    border-radius: 0 0 1em 1em;
    z-index: 3;
  }

  @media screen and (max-width: 1122px) {
  }

  @media screen and (max-width: 700px) {
    h3 {
      font-size: 20vw;
    }

    li {
      display: flex;
      position: relative;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      text-decoration: none;
      list-style: none;
      font-size: 10vw;
      padding: 1px;
      padding: 1% 2%;
      transition: 0.3s;
      overflow: hidden;
    }
    
    li:first-child {
      border-top: solid 1px var(--gunMetal);
    }
    
    li img {
      display: none;
    }
    
    .date2 {
      position: absolute;
      right: 2%;
      bottom: 0.8em;
      display: none;
    }
    
    .tags {
      position: relative;
      top: 30%;
      left: 0;
      gap: 0.2em;
      margin: 1% 0 1.5% 0;
    }
    
    .tag {
      font-size: .7rem;
      padding: 0.2em .8em;
      border-radius: 1em;
      font-weight: 300;
    }
  }
</style>
