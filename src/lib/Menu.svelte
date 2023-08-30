<script>
  import { gsap } from "gsap";
  import { onMount } from "svelte";
  import arrow from '$lib/assets/arrow.svg';
  


  onMount(() => {
    let menuButton = document.querySelector(".menu-button");
    let contactLink = document.querySelector(".contact-link");

    const projects = document.querySelector(".projects");

    projects.addEventListener("click", (e) => {
      e.preventDefault();
      goToPage("/projects");
    });

    const goToPage = (url) => {
      gsap.to(".transition", {
        y: "-10%",
        rotate: 0,
        delay: 0,
        stagger: 0,
        duration: 1,
      });
      setTimeout(() => {
        window.location.href = url;
      }, 1000);
    };

    let mm = gsap.matchMedia();

    let tl = gsap.timeline({ paused: true, reversed: true });
    tl.to(".menu-wrapper", {
      width: "60%",
      borderRadius: "1em",
      duration: 1.2,
      ease: "Expo.easeInOut",
    });

    mm.add("(max-width: 700px)", () => {
      tl.to(
        ".menu-wrapper",
        {
          width: "94%",
          borderRadius: "1em",
          duration: 1.2,
          ease: "Expo.easeInOut",
          delay: 0,
        },
        "<"
      );
    });

    tl.to(
      ".explore",
      { y: 0, duration: 2, ease: "Expo.easeInOut", delay: 1 },
      "<"
    );
    tl.to(
      ".menu-wrapper",
      { height: "96svh", duration: 1.2, ease: "Expo.easeOut", delay: 0.1 },
      "<"
    );
    tl.to(
      "button img",
      { rotate: 360, x: -6, duration: 1.5, ease: "Expo.easeInOut", delay: 0 },
      "<"
    );
    tl.to(
      ".menu-text-gsap",
      { y: 0, duration: 2, ease: "Expo.easeOut", delay: 0.6 },
      "<"
    );
    tl.to(".number", { y: 0, duration: 1.7, ease: "Expo.easeOut" }, "<");
    tl.to(
      ".socials-gsap",
      { y: 0, duration: 1.5, stagger: 0.2, delay: 0.4, ease: "Expo.easeInOut" },
      "<"
    );

    menuButton.addEventListener("click", function () {
      if (tl.reversed()) {
        tl.timeScale(1.5).play();
      } else {
        tl.timeScale(1.5).reverse();
      }
    });

    contactLink.addEventListener("click", function (e) {
      e.preventDefault();
      tl.timeScale(1.5).reverse();
      setTimeout(function () {
        window.location.href = "#contact";
      }, 1800);
    });

  });
</script>

<section>
  <div class="menu-wrapper">
    <div class="button-wrapper">
    <button class="menu-button">
        <img src={arrow} alt="Menu arrow" /></button
    >
  </div>
    <h3 class="explore">
      Explore
    </h3>
    <nav>
      <ul>
        <li>
          <p class="number">01</p>
          <a class="menu-text-gsap" href="https://studiorolie.com#about">About</a>
        </li>
        <li>
          <p class="number">02</p>
          <a class="menu-text-gsap projects" href="/projects">Projects</a>
        </li>
        <li>
          <p class="number">03</p>
          <a class="menu-text-gsap" href=" ">Coming soon</a>
        </li>
        <li>
          <p class="number">04</p>
          <a class="menu-text-gsap contact-link" href="#contact"
            >Contact</a
          >
        </li>
      </ul>
    </nav>

    <div class="submenu">
      <div class="left-submenu socials-gsap">
        <p class="subhead">Contact</p>
        <ul class="socials">
          <li>
            <a href="mailto:contact@studiorolie.com"
              >contact@studiorolie.com</a
            >
            <a href="tel:+31 653 63 51 06">+31 653 63 51 06</a>
          </li>
        </ul>
      </div>
      <div class="right-submenu socials-gsap">
        <p class="subhead">socials</p>
        <ul class="socials">
          <li><a href="https://www.instagram.com/studiorolie/">Instagram</a></li>
          <li><a href="https://www.linkedin.com/in/milan-rolie-778150151//">LinkedIn</a></li>
          <li><a href="https://github.com/milanrolie">GitHub</a></li>
        </ul>
      </div>
    </div>
  </div>
</section>

<style>
  .menu-wrapper {
    position: fixed;
    right: 1%;
    top: 1em;
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

  .button-wrapper {
    position: absolute;
    top: 0;
    right: 0;
    width: max-content;
    height: auto;
  }
  
  button {
    position: relative;
    background-color: rgba(255, 255, 255, 0);
    padding: 1.5em;
    border: 0;
    z-index: 12;
    transition: transform 0.2s;
  }

  button:hover {
    cursor: pointer;
  }
  
  button:hover button img {
    transform: rotate(135deg);
  }

  button img {
    position: absolute;
    top: .5em;
    left: .9em;
  }

  img {
    height: 2em;
    width: 2em;
    transform: rotate(180deg);
  }

  nav li {
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
    transform: translateY(-130%);
    transition: margin 0.2s;
  }

  nav a:hover {
    color: var(--webLavender);
    margin-left: 1%;
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

  .socials a {
    margin-right: 2em;
  }

  @media screen and (max-width: 1122px) {
  }

  @media screen and (max-width: 700px) {
    .menu-wrapper {
      top: 1.5%;
      right: 3%;
    }


  button img {
    position: absolute;
    top: 8px;
    left: 8px;
  }

    nav {
      margin-top: 10%;
    }

    nav a {
      margin-top: 3%;
      font-size: 13vw;
    }

    .submenu {
      position: absolute;
      right: 0.5em;
      bottom: -1em;
    }

    .socials a {
      font-size: 0.8em;
    }
  }
</style>
