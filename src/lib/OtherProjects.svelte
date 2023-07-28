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
    const hoverElement5 = document.querySelector(".fifth");
    const projectImage5 = document.querySelector(".project-image5");
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

    hoverElement5.addEventListener("mouseenter", () => {
      projectImage5.classList.toggle("view");
    });

    hoverElement5.addEventListener("mouseleave", () => {
      projectImage5.classList.toggle("view");
    });

    hoverElement6.addEventListener("mouseenter", () => {
      projectImage6.classList.toggle("view");
    });

    hoverElement6.addEventListener("mouseleave", () => {
      projectImage6.classList.toggle("view");
    });
  });
</script>

<section>
  <div class="wrapper">
    <div class="clip">
      <h3 class="others-gsap">others</h3>
    </div>
    <ul>
      <a href="https://studiorolie.com/a-better-planet">
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
      <a href="https://studiorolie.com/ink">
        <li class="first">
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
      <a href="https://studiorolie.com/markk">
        <li class="first">
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
      <a href="https://studiorolie.com/ubica">
        <li class="first">
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
      <a href="https://studiorolie.com/commentary-tool">
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
      </a>
      <a href="https://studiorolie.com/family-fitness">
        <li class="third">
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
      </a>
      <a href="https://studiorolie.com/challem">
        <li class="fourth">
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
      <a href="https://studiorolie.com/twintig">
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
      </a>
      <a href="https://studiorolie.com/squad-page">
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
      </a>
    </ul>
    <div class="image-wrapper">
      <img class="project-image project-image" src={markk} alt="" />

      <img class="project-image project-image1 view" src={highTea} alt="" />

      <img class="project-image project-image2 view" src={commentary} alt="" />

      <img class="project-image project-image3 view" src={fitness} alt="" />

      <img class="project-image project-image4 view" src={challem} alt="" />

      <img class="project-image project-image5 view" src={twintig} alt="" />

      <img class="project-image project-image6 view" src={squad} alt="" />
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
    border-top: solid 1px var(--gunMetal);
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

  li:last-child {
    border-bottom: solid 1px var(--gunMetal);
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
      font-size: 7vw;
      border-top: solid 1px var(--gunMetal);
      padding: 1px;
      padding: 1% 2%;
      transition: 0.3s;
      overflow: hidden;
    }

    .date2 {
      position: absolute;
      right: 2%;
      bottom: 0.8em;
    }

    .tags {
      position: relative;
      top: 30%;
      left: 0;
      gap: 0.2em;
      margin: 1% 0 1.5% 0;
    }

    .tag {
      background-color: none;
      font-size: 0.3em;
      padding: 0.3em 1em;
      border-radius: 1em;
      text-decoration: none;
      color: var(--gunMetal);
      text-transform: uppercase;
      border: solid 1px var(--gunMetal);
      transform: translateX(50px);
      opacity: 0;
    }
  }
</style>
