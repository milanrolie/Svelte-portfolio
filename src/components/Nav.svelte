
<script>
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger"
 	import { onMount } from "svelte";

    gsap.registerPlugin(ScrollTrigger)


onMount(() => {
    gsap.from(".gsap", {
    y: -200, 
    delay: 1.5,
    stagger: 0,
    duration: 1
});

gsap.to(".hello", {
    y: 0,
    delay: 1.5, 
    duration: 1
});

gsap.to("nav", {
    scrollTrigger: {
        trigger: 'nav',
        scrub: 1,
        start: 'top top',
    },
    y: -100,
});

});

</script>

<nav>
<h2 class="logo-text gsap">Studio Rolie</h2>
    <ul class="gsap">
        <li>About</li>
        <li>my Work</li>
        <li>Contact</li>
    </ul>
    <button class="hello"> Say Hello</button>
</nav>

<style>
    nav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 100%;
        padding: 1em;
        position: fixed;
        z-index: 10;
    }

    ul {
        display: flex;
        flex-direction: column;
    }

    li{
        list-style-type: none;
        color: var(--dark);
        text-transform: uppercase;
        letter-spacing: 2px;
        font-weight: 200;
    }


    li:hover {
        color: var(--webLavender);
        cursor: pointer;
    }

    .logo-text {
        color: var(--dark);
        text-transform: uppercase;
        font-weight: 600;
        cursor: pointer;
    }

    button {
        padding: 10px 2em;
        border-radius: 3em;
        font-family: 'Outfit', sans-serif;
        font-size: .8em;
        letter-spacing: 2px;
        text-transform: uppercase;
        border: none;
        transition: opacity .2s;
        cursor: pointer;
        height: max-content;
        transform: translateY(-200px);
    }

    button:hover {
        background-color: var(--justBlue);
    }
</style>