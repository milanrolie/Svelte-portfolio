<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";
  import arrow from '$lib/assets/arrow.svg';

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
      stagger: .4,
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
      stagger: .1,
      scrollTrigger: {
        trigger: ".clip",
        start: "top-=600",
        end: "top-=100",
        toggleActions: "play none none none",
        // markers: true,
      },
    });

    const hoverElement1 = document.querySelector('.first')
    const projectImage1 = document.querySelector('.project-image1')
    const hoverElement2 = document.querySelector('.second')
    const projectImage2 = document.querySelector('.project-image2')


    hoverElement1.addEventListener("mouseenter", () => {
      projectImage1.classList.toggle('view')
    })

    hoverElement1.addEventListener("mouseleave", () => {
      projectImage1.classList.toggle('view')
    })


    hoverElement2.addEventListener("mouseenter", () => {
      projectImage2.classList.toggle('view')
    })

    hoverElement2.addEventListener("mouseleave", () => {
      projectImage2.classList.toggle('view')
    })


    // toggleFullscreen.addEventListener("click", () => {


  });
</script>

<section>
  <div class="wrapper">
    <div class="clip">
      <h3 class="others-gsap">others</h3>
    </div>
    <ul>
      <li class="first">
        <div class="clip">
          <p class="allProjects-gsap">
            Project over iets <img src="{arrow}" alt="" />
          </p>
        </div>
        <div class="tags">
        <p class="tag"> Website </p>
        <p class="tag"> video </p>
      </div>

        <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
      <li class="second" >
        <div class="clip">
          <p class="allProjects-gsap">
            50k for a better planet <img src="{arrow}" alt="" />
          </p>
        </div>
        <div class="tags">
          <p class="tag"> Website </p>
          <p class="tag"> design </p>
          <p class="tag"> Animations </p>
        </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
      <li>
        <div class="clip">
          <p class="allProjects-gsap">
            Commentary tool <img src="{arrow}" alt="" />
          </p>
        </div>
        <div class="tags">
          <p class="tag"> Website </p>
          <p class="tag"> design </p>
          <p class="tag"> ux </p>
        </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
      <li>
        <div class="clip">
          <p class="allProjects-gsap">
            Project over iets <img src="{arrow}" alt="" />
          </p>
        </div>
        <div class="tags">
          <p class="tag"> Website </p>
          <p class="tag"> design </p>
          <p class="tag"> ux </p>
        </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
      <li>
        <div class="clip">
          <p class="allProjects-gsap">
            over iets Anders <img src="{arrow}" alt="" />
          </p>
        </div>
        <div class="tags">
          <p class="tag"> Website </p>
          <p class="tag"> design </p>
          <p class="tag"> ux </p>
        </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
      <li>
        <div class="clip">
          <p class="allProjects-gsap">
            Ink Rio de Janeiro <img src="{arrow}" alt="" />
          </p>
        </div>
        <div class="tags">
          <p class="tag"> Website </p>
          <p class="tag"> design </p>
          <p class="tag"> ux </p>
        </div>
          <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
    </ul>
    <div class="image-wrapper">
      <img
        class="project-image project-image1 view"
        src="https://images.unsplash.com/photo-1523274158540-2aa98c15ec26?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80"
        alt=""
      />

      <img
      class="project-image project-image2 view"
      src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2069&q=80"
      alt=""
    />
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
    gap: .5em;
  }

  .tag {
    background-color: none;
    font-size: .4em;
    padding: .3em 1em;
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
    right: -1em;
    height: 2.6vw;
    width: 2.6vw;
    transform: translateY(10px);
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
    transition: .5s;
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
    opacity: 0.5;
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
    bottom: .8em;
  }

  .tags {
    position: relative;
    top: 30%;
    left: 0;
    gap: .2em;
    margin: 1% 0 1.5% 0;
  }

  .tag {
    background-color: none;
    font-size: .3em;
    padding: .3em 1em;
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
