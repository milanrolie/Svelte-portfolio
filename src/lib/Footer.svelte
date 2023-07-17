<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    gsap.from(".stagger", {
      scrollTrigger: {
        trigger: "footer",
        scrub: 1,
        start: "top-=700",
        end: "top-=400",
      },
      y: 300,
      opacity: 0.5,
    });
  });
</script>

<footer id="footer-scroll">
  <div class="wrapper">
    <div class="left-content">
      <ul class="stagger">
        <li>Milan Rolie</li>
        <li>
          Creative developer <br /> <span class="designer">& designer </span>
        </li>
      </ul>
    </div>
    <div class="center-content">
      <ul class="stagger">
        <li>Based in Utrecht,</li>
        <li>The Netherlands</li>
      </ul>
    </div>
    <div class="right-content">
      <ul class="stagger">
        <li>Nog iets leuks?</li>
        <li>Komt nog wel?</li>
      </ul>
    </div>
  </div>
  <div class="big-mailto stagger">
    <a class="big-mail-text" href="mailto: contact@studiorolie.com"
      >contact<br class="footer-br" />@studiorolie.com
      <div class="svg-box">
        <svg
          class="svg1"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          ><path
            d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"
          /></svg
        >
        <!-- <svg class="svg2" xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path d="M7 7h8.586L5.293 17.293l1.414 1.414L17 8.414V17h2V5H7v2z"/></svg> -->
      </div>
    </a>
  </div>
  <ul class="socials stagger">
    <li><a href="https://www.instagram.com/milanrolie/">Instagram</a></li>
    <li>Behance</li>
    <li>LinkedIn</li>
    <li>Facebook</li>
  </ul>
</footer>

<style>
  footer {
    height: 50vh;
    background-color: var(--gunMetal);
    padding: 0% 2%;
  }

  .wrapper {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: flex-start;
    justify-content: space-between;
    padding-right: 20%;
  }

  li {
    text-decoration: none;
    list-style: none;
  }

  a {
    text-decoration: none;
    color: var(--bitterSweet);
  }

  .big-mail-text {
    position: relative;
    margin-top: 1em;
    font-size: 6vw;
    color: var(--bitterSweet);
    text-decoration: none;
    display: flex;
    flex-direction: row;
    width: max-content;
  }

  .designer {
    margin-left: 44%;
  }

  .big-mail-text:hover svg {
    transform: translateX(25%) translateY(-25%);
  }

  .svg-box {
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    position: absolute;
    top: 35%;
    right: -3%;
    max-height: 20px;
    max-width: 20px;
    /* background-color: aqua; */
    /* overflow: hidden; */
  }

  svg {
    fill: var(--bitterSweet);
    transition: 0.8s;
  }

  svg:hover {
    transform: translateX(70%) translateY(-70%);
  }

  .socials {
    display: flex;
    flex-direction: row;
    gap: 2em;
    margin-top: 1em;
  }

  .socials li {
    color: var(--bitterSweet);
    letter-spacing: 1px;
    padding: 0px 4px;
    padding-top: 1px;
    transition: 0.2s;
    cursor: pointer;
    font-size: clamp(10px, 1vw, 2em);
  }

  .socials li:hover {
    transform: translateX(2px);
  }

  .footer-br {
    display: none;
  }

  @media screen and (max-width: 1122px) {
  }

  @media screen and (max-width: 700px) {
    .footer-br {
      display: block;
    }

    .big-mail-text {
        font-size: 12vw;
        line-height: 1em;
    }

    .socials {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(2, 1fr);
      grid-column-gap: 0px;
      grid-row-gap: 0px;
      max-width: 40%;
      gap: 0.5em;
    }

    .socials li {
        font-size: 1em;
    }
  }
</style>
