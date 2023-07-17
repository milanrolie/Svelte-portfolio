<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    let menuButton = document.querySelector('.menu-button')

    let tl = gsap.timeline({ paused: true, reversed: true });
    tl.to(".menu-wrapper", {
      width: "60%",
      borderRadius: "1em",
      duration: 1.2,
      ease: "Expo.easeInOut",
    });
    tl.to(".explore",{ y:0, duration: 2, ease: "Expo.easeInOut", delay: 1 },"<");
    tl.to(".menu-wrapper",{ height: "96vh", duration: 1.2, ease: "Expo.easeOut", delay: .1 },"<");
    tl.to(".menu-button", { rotate: 270, duration: .8, ease: "Expo.easeInOut", delay: 0 }, "<");
    tl.to(".menu-text-gsap",{ y: 0, duration: 2, ease: "Expo.easeOut", delay: 0.6 },"<");
    tl.to(".number", { y: 0, duration: 1.7, ease: "Expo.easeOut" }, "<");
    tl.to(".socials-gsap", { y: 0, duration: 1.5, ease: "Expo.easeInOut", stagger: .2, delay: .4 }, "<");

    menuButton.addEventListener('click', function () {
        if (tl.reversed()) {
            tl.timeScale(1.5).play();
        } else {
            tl.timeScale(1.5).reverse();
        }
    })
  });
</script>
<section>
    <div class="menu-wrapper">
    <button class="menu-button"> <img src="src/assets/arrow.svg" alt=""></button>
  <h3 class="explore">
    Explore <img src="src/assets/arrow.svg" alt="">
  </h3>
  <!-- <button class="close-button">close</button> -->
  <nav>
    <ul>
      <li>
        <p class="number">01</p>
        <a class="menu-text-gsap" href="">About</a>
      </li>
      <li>
        <p class="number">02</p>
        <a class="menu-text-gsap" href="">Projects</a>
      </li>
      <li>
        <p class="number">03</p>
        <a class="menu-text-gsap" href="">Photography</a>
      </li>
      <li>
        <p class="number">04</p>
        <a class="menu-text-gsap" href="">Contact</a>
      </li>
    </ul>
  </nav>

  <div class="submenu">
    <div class="left-submenu socials-gsap">
      <p class="subhead">Contact</p>
      <ul class="socials">
        <li>
          <a href="https://www.instagram.com/milanrolie/">contact@studiorolie.com</a>
          <a href="https://www.instagram.com/milanrolie/">+31 653 63 51 06</a>

        </li>
      </ul>
    </div>
    <div class="right-submenu socials-gsap">
      <p class="subhead">socials</p>
      <ul class="socials">
        <li><a href="https://www.instagram.com/milanrolie/">Instagram</a></li>
        <li>Behance</li>
        <li>LinkedIn</li>
        <li>Github</li>
      </ul>
    </div>
  </div>
</div>
</section>

<style>
  .menu-wrapper {
    position: fixed;
    right: 1%;
    top: 2%;
    height: 10px;
    width: 10px;
    display: flex;
    flex-direction: column;
    background-color: rgb(20, 20, 20);
    padding: 1.1em;
    border-radius: 5em;
    z-index: 8;
    overflow: hidden;
    background: rgba(20, 20, 20, 0.85);
    backdrop-filter: blur(15px);
    -webkit-backdrop-filter: blur(15px);
  }

  h3 {
    color: var(--gunMetal);
    font-family: var(--font2);
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 5%;
  }

  .explore {
    transform: translateY(-400%);
  }

  /* button {
    position: absolute;
    top: 1em;
    right: 1em;
    padding: 0.5em 1em;
    border-radius: 3em;
    border: none;
    font-family: "Outfit", sans-serif;
    letter-spacing: 1px;
    text-transform: uppercase;
    font-weight: 500;
    transform: translateX(130%);
  } */

  button {
    position: fixed;
    top: -2px;
    right: 0;
    background-color: rgba(255, 255, 255, 0);
    padding: 1em;
    border: 0;
    z-index: 12;
    transform: rotate(90deg) scale(1.8);
    transition: transform 0.2s;
  }

  button:hover {
    cursor: pointer;
    transform: rotate(135deg) scale(1.8);
  }


  nav {
  }

  ul {
  }

  img {
    height: .9em;
    transform: rotate(90deg);
  }

  nav li {
    /* border-bottom: solid 1px var(--gunMetal); */
    list-style-type: none;
    display: flex;
    flex-direction: row;
    gap: 1em;
    align-items: baseline;
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
  }

  .number {
    transform: translateY(300%);
  }

  p {
    color: var(--gunMetal);
    font-size: 1em;
  }
  a {
    text-decoration: none;
    color: var(--gunMetal);
  }
  nav a {
    font-size: 5em;
    transform: translateY(-100%);
  }

  .submenu {
    position: absolute;
    right: 3em;
    bottom: 0;
    display: flex;
    flex-direction: row;
    gap: 1em;
    margin-left: 3em;
  }

  .subhead {
    letter-spacing: 1px;
    text-transform: uppercase;
    font-size: 0.7em;
    font-weight: 600;
    margin-bottom: 5px;
  }

  .socials {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    list-style-type: none;
    color: var(--gunMetal);
    max-width: 50%;
  }

  .socials-gsap {
    transform: translateY(200%);
  }

  .left-submenu {
    /* max-width: 50%; */
  }

  .socials a {
    margin-right: 2em;
  }
</style>
