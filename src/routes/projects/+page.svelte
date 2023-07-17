<script>
  import Nav from "$lib/Nav.svelte";
  import OtherProjects from "$lib/OtherProjects.svelte";
  import Footer from "$lib/Footer.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.from(".projects", {
      y: 900,
      delay: 1,
      duration: 1.5,
      ease: "power4.out",
    });

    gsap.from(".case", {
      y: 700,
      delay: 1.2,
      duration: 1.5,
      stagger: 0.2,
      ease: "power4.out",
    });

    gsap.from(".svg2", {
      y: 500,
      delay: 2,
      duration: 1.5,
      ease: "power4.out",
    });
  });
</script>

<Nav />

<section class="cases">
  <h1 class="projects">all projects <svg
    class="svg2"
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    ><path
      d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
    /></svg></h1>

  <div class="projects-wrapper">
    <div class="case">
      <a href="https://ubicautrecht.nl/" target="_blank">
        <div class="image-clip">
        <img
          class="first-project-image"
          src="https://twintig-utrecht.nl/wp-content/uploads/2022/01/Ubica-NSlagmolen-29-september-202119-scaled.jpg"
          alt="test"
          width="400"
          height="400"
        />
        </div>

        <div class="subscript">
          <p class="view-project black">Ubica Utrecht</p>
          <p class="animated-tags">Website / design / work</p>

          <svg
            class="svg1"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            ><path
              d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
            /></svg
          >
        </div>
      </a>
    </div>
    <div class="case">
      <a href="https://ubicautrecht.nl/" target="_blank">
        <div class="image-clip">
        <img
          src="https://images.unsplash.com/photo-1525286335722-c30c6b5df541?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80"
          alt="test"
          width="400"
          height="400"
        />
        </div>

        <div class="subscript">
          <p class="view-project black">Ubica Utrecht</p>

          <svg
            class="svg1"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            ><path
              d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
            /></svg
          >
        </div>
      </a>
    </div>
    <div class="case">
        <a href="https://ubicautrecht.nl/" target="_blank">
          <div class="image-clip">
          <img
            class="first-project-image"
            src="https://twintig-utrecht.nl/wp-content/uploads/2022/01/Ubica-NSlagmolen-29-september-202119-scaled.jpg"
            alt="test"
            width="400"
            height="400"
          />
          </div>
  
          <div class="subscript">
            <p class="view-project black">Ubica Utrecht</p>
            <p class="animated-tags">Website / design / work</p>
  
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              ><path
                d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
              /></svg
            >
          </div>
        </a>
      </div>
      <div class="case">
        <a href="https://ubicautrecht.nl/" target="_blank">
          <div class="image-clip">
          <img
            src="https://images.unsplash.com/photo-1525286335722-c30c6b5df541?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80"
            alt="test"
            width="400"
            height="400"
          />
          </div>
  
          <div class="subscript">
            <p class="view-project black">Ubica Utrecht</p>
  
            <svg
              class="svg1"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              ><path
                d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
              /></svg
            >
          </div>
        </a>
      </div>
  


    <Footer />
  </div>
</section>

<style>
  .cases {
    padding-top: 10%;
  }

  h1 {
    text-transform: capitalize;
    margin-bottom: 2%;
    font-family: var(--font2);
    letter-spacing: 1;
    padding-bottom: 2%;
    border-bottom: solid 1px var(--dark);
  }

  .svg2 {
    position: absolute;
    transform: scale(2) rotate(180deg);
    bottom: 14%;
    right: 1%;
  }

  .projects-wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%;
    gap: 2%;
  }

  .case {
    position: relative;
    width: 49%;
    margin-bottom: 5%;
}

.image-clip {
      clip-path: inset(0px 0px 1% 0px round 1em);
  }

  img {
    aspect-ratio: 1.3;
    width: 100%;
    height: auto;
    transition: .5s;
}

.subscript {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 0 1px;
    border-bottom: 1px solid var(--dark);
    overflow: hidden;
  }

  .animated-tags {
    transform: translateX(200%);
    transition: 0.6s;
  }
  .case:hover .animated-tags {
    transform: translateX(10%);
  }

  .svg1 {
    transition: .3s;
  }

  .case:hover .svg1 {
    transform: rotate(45deg);
  }

  .case:hover img {
    transform: scale(1.1);
  }

  a {
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;
  }




</style>
