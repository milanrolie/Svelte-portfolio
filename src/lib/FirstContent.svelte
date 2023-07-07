<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.from(".intro-gsap", {
        y: 300,
        stagger: 0.1,
        delay: 2.5,
        duration: 1,
        ease: "power4.out",
    });

    const tl = new gsap.timeline({
        scrollTrigger: {
            trigger: ".image-wrapper",
            scrub: 1,
            start: "top-=800",
            end: "bottom+=100",
            // markers: true,
        },
        stagger: 0.5,
        
    })

    tl.to('.img1', {y: -400}, "img")
    .to('.img2', {y: -300, },"img")
    .to('.img3', {y: -200, },"img")
  });
</script>

<section class="image-wrapper">
  <img
    class="img1 intro-gsap"
    src="https://milanrolie.com/wp-content/uploads/2021/02/abri.png"
    alt="test"
  />
  <img
    class="img2 intro-gsap"
    src="../src/assets/markk.png"
    alt="test"
  />
  <img
    class="img3 intro-gsap"
    src="src/assets/phone.jpg"
    alt="test"
  />
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

</style>
