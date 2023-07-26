<script>
  import Menu from "../lib/Menu.svelte";
  import IntroAnimatie from "../lib/IntroAnimatie.svelte";
  import Nav from "../lib/Nav.svelte";
  import Nested from "../lib/Nested.svelte";
  import FirstContent from "../lib/FirstContent.svelte";
  import About from "../lib/About.svelte";
  import ProjectOne from "../lib/ProjectOne.svelte";
  import BigImage from "../lib/BigImage.svelte";
  import Cases from "../lib/Cases.svelte";
  import Marquee from "../lib/Marquee.svelte";
  import Footer from "../lib/Footer.svelte";
  import Contact from "../lib/Contact.svelte";
  import Transition from "../lib/Transition.svelte";
  import OtherProjects from "../lib/OtherProjects.svelte";
  import AllProjects from "../lib/allProjects.svelte";

  import { onMount } from "svelte";
  import Lenis from "@studio-freight/lenis";

  onMount(() => {
    const lenis = new Lenis({
      duration: 1.5,
      easing: (t) => (t === 1 ? 1 : 1 - Math.pow(2, -10 * t)),
      direction: "vertical",
      gestureDirection: "vertical",
      smooth: true,
      smoothTouch: false,
      touchMultiplier: 2,
    });

    function raf(time) {
      lenis.raf(time);
      requestAnimationFrame(raf);
    }

    requestAnimationFrame(raf);

    lenis.on("scroll", (e) => {
      console.log(e);
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
  });
</script>

<Transition />
<IntroAnimatie />
<Nav />
<Menu />
<Nested />
<!-- <FirstContent /> -->
<!-- <BigImage /> -->
<About />
<Cases />
<!-- <Contact />zx -->
<!-- <OtherProjects /> -->
<AllProjects />
<Marquee />
<Footer />

<!-- <ProjectOne /> -->

<style>
  @import url("https://fonts.googleapis.com/css2?family=Outfit:wght@100;300;400;500;600;700;800;900&display=swap");
</style>
