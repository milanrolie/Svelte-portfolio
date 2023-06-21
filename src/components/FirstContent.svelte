<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.from(".intro-gsap", {
        y: 500,
        stagger: 0.1,
        delay: 1,
        duration: 1,
        ease: "power4.out",
    });

    // gsap.to(".img1", {
    //   scrollTrigger: {
    //     trigger: "img1",
    //     scrub: 1,
    //     start: "top",
    //     end: "+=100",
    //     // markers: true,
    //   },
    //   y: -100,
    // });

    const tl = new gsap.timeline({
        scrollTrigger: {
            trigger: ".image-wrapper",
            scrub: 1,
            start: "top-=500",
            end: "bottom+=100",
            // markers: true,
        },
        stagger: 0.2,
        
    })

    tl.fromTo('.img1', {y: 0}, {y: -500}, "img")
    .fromTo('.img2', {y: 0}, {y: -500, delay: 0.05},"img")
    .fromTo('.img3', {y: 0}, {y: -500, delay: 0.1},"img")

    // gsap.fromTo('img1', {
    //     y: 500
    // }, {
    //     y: 300,
    //     scrollTrigger: {
    //         trigger: ".img1",
    //         scrub: 1,
    //         start: "top",
    //         end: "bottom+=100",
    //         markers: true,
    //     }
    // })

    // gsap.to(".img2", {
    //   scrollTrigger: {
    //     trigger: "img2",
    //     scrub: 1,
    //     start: "top",
    //     end: "+=100",
    //     // markers: true,
    //   },
    //   y: -500,
    // });

    // gsap.to(".img3", {
    //   scrollTrigger: {
    //     trigger: "img3",
    //     scrub: 1,
    //     start: "top",
    //     end: "+=100",
    //     // markers: true,
    //   },
    //   y: -200,
    // });
  });
</script>

<section class="image-wrapper">
  <img
    class="img1 intro-gsap"
    src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/06/iphone-14-pro-black-free-mockup-1072x0-c-default.jpg"
    alt="test"
  />
  <img
    class="img2 intro-gsap"
    src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/05/urban-posters-free-mockup-psd-1072x0-c-default.jpg"
    alt="test"
  />
  <img
    class="img3 intro-gsap"
    src="https://images.unsplash.com/photo-1587938745570-681161dcfe17?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=983&q=80"
    alt="test"
  />
</section>

<style>
  .image-wrapper {
    width: 100%;
    display: flex;
    flex-direction: row;
    gap: 2%;
  }

  img {
    width: 32%;
    height: 70vh;
    object-fit: cover;
    border-radius: 1em;
    /* transform: translateY(-200px); */
  }
</style>
