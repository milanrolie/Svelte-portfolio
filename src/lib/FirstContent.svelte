<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.to(".intro-gsap", {
      y: 0,
      stagger: 0.1,
      delay: 5.5,
      duration: 1,
      ease: "power4.out",
    });

    const tl = new gsap.timeline({
      scrollTrigger: {
        trigger: "nav",
        scrub: 1,
        start: "top",
        end: "bottom+=500",
        // markers: true,
      },
      stagger: 0.5,
    });

    let mm = gsap.matchMedia();

    // add a media query. When it matches, the associated function will run
    mm.add("(min-width: 1200px)", () => {
      tl.to(".img1", { y: -400 }, "img")
        .to(".img2", { y: -300 }, "img")
        .to(".img3", { y: -200 }, "img");
    });
  });
</script>

<section class="image-wrapper">
  <img
    class="img1 intro-gsap case"
    src="https://images.unsplash.com/photo-1479839672679-a46483c0e7c8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1010&q=80"
    alt="test"
  />
  <img class="img2 intro-gsap" src="../src/assets/markk.png" alt="test" />
  <img class="img3 intro-gsap" src="src/assets/phone.jpg" alt="test" />
</section>

<style>
  .image-wrapper {
    position: relative;
    width: 100%;
    height: 70vh;
    display: flex;
    flex-direction: row;
    gap: 2%;
  }

  img {
    width: 32%;
    height: 70vh;
    object-fit: cover;
    border-radius: 1em;
    transform: translateY(0px);
  }

  .intro-gsap {
    transform: translateY(500px);
  }

  @media screen and (max-width: 1122px) {
    .img3 {
      display: none;
    }

    img {
      width: 49%;
      height: 65vh;
    }
  }

  @media screen and (max-width: 700px) {
    .image-wrapper {
      position: relative;
      width: 100%;
      height: max-content;
      display: flex;
      flex-direction: row;
      gap: 2%;
    }

    .img2 {
      display: none;
    }

    img {
      width: 100%;
      height: 120%;
    }
  }
</style>
