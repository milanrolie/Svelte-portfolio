<script>
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger"
 	import { onMount } from "svelte";

    gsap.registerPlugin(ScrollTrigger)



onMount(() => {
    gsap.to(".big-image", {
    scrollTrigger: {
        trigger: '.big-image',
        scrub: 1,
        start: 'top-=700',
        end: 'top+=300',
        markers: true,
    },
    y: -100,
    '--progress': 1
});
});


</script>

<section>
<img class="big-image" src="src/assets/aarhus.jpg" alt="">
</section>

<style>
    section{
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 0;
    }

    img {
        object-fit: cover;
        height: 70vh;
        width: 110%;
        clip-path: inset(0 calc((1 - var(--progress)) * 20%) 0 calc((1 - var(--progress)) * 20%) round 1em);
    }

    @media screen and (max-width: 1122px) {
    section {
        display: none;
    }
  }
</style>
