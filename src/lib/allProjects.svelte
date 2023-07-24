<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

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

  });
</script>

<section>
  <div class="wrapper">
    <div class="clip">
      <h3 class="others-gsap">others</h3>
    </div>
    <ul>
      <li>
        <div class="clip">
          <p class="allProjects-gsap">
            Project over iets <img src="src/assets/arrow.svg" alt="" />
          </p>
        </div>
        <div class="tags">
        <p class="tag"> Website </p>
        <p class="tag"> video </p>
      </div>

        <p class="date2 allRight-gsap">10-11-2019</p>
      </li>
      <li>
        <div class="clip">
          <p class="allProjects-gsap">
            50k for a better planet <img src="src/assets/arrow.svg" alt="" />
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
            Commentary tool <img src="src/assets/arrow.svg" alt="" />
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
            Project over iets <img src="src/assets/arrow.svg" alt="" />
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
            over iets Anders <img src="src/assets/arrow.svg" alt="" />
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
            Ink Rio de Janeiro <img src="src/assets/arrow.svg" alt="" />
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
        class="project-image"
        src="https://images.unsplash.com/photo-1523274158540-2aa98c15ec26?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80"
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

  .allRight-gsap {
  }

  /* .colored {
    position: absolute;
    left: 0;
    top: -100%;
    background-color: rgb(202, 202, 202);
    width: 100%;
    height: 100%;
    z-index: -1;
    transition: cubic-bezier(1, 0, 0.49, 1.02) 0.8s;
  } */

  li:hover .colored {
    transform: translateY(100%);
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
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 0 0 1em 1em;
    z-index: 2;
  }

  .image-overlay {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: var(--dark);
    opacity: 0.8;
    border-radius: 0 0 1em 1em;
    z-index: 3;
  }
</style>
