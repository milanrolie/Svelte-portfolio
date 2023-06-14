<script>
  import Nav from "../components/Nav.svelte";
  import Nested from "../components/Nested.svelte";
  import FirstContent from "../components/FirstContent.svelte";
  import About from "../components/About.svelte";
  import ProjectOne from "../components/ProjectOne.svelte";
  import BigImage from "../components/BigImage.svelte";
  import Cases from "../components/Cases.svelte";
  import Marquee from "../components/Marquee.svelte";
  import Footer from "../components/Footer.svelte";



  import Contact from "../components/Contact.svelte";





</script>

<Nav />
<Nested />
<FirstContent />
<About />
<BigImage />
<Cases />
<Marquee />
<Contact />
<Footer />




<!-- <ProjectOne /> -->


<style>
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@100;300;400;500;600;700;800;900&display=swap');

:global(:root) {
    --flashWhite: #E9ECEB;
    --gunMetal: #11110f;
    --justBlue: #774ff0;
    --bitterSweet: #FE5F55;
    --webLavender: #bed0fa;
}

  :global(*) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :global(body) {
    background-color: var(--gunMetal);
    font-family: 'Outfit', sans-serif;
    overflow-x: hidden;
  }
  
  :global(section) {
    padding: 0% 2%;
  }

  :global(h1) {
    color: var(--flashWhite);
    text-transform: uppercase;
    font-size: 6vw;
    font-weight: 300;
    line-height: 1em;
  }

  :global(h2) {
    font-size: 2em;
    font-weight: 700;
  }

  :global(img) {
    border-radius: .5em;
  }

  :global(p) {
    color: var(--flashWhite);
  }
  
</style>
