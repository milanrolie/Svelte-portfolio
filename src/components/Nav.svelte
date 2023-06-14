
<script>
//     import { gsap } from "gsap";
// 	import { onMount } from "svelte";


// onMount(() => {
//     gsap.from(".gsap", {
//     x: 200, 
//     duration: 1});
// });

</script>

<nav class="gsap">
<h2 class="logo-text">Studio Rolie</h2>
    <ul>
        <li>About</li>
        <li>my Work</li>
        <li>Contact</li>
    </ul>
    <button>Say Hello</button>
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
        color: var(--flashWhite);
        text-transform: uppercase;
        letter-spacing: 2px;
        font-weight: 200;
    }

    li:hover {
        color: var(--webLavender);
        cursor: pointer;
    }

    .logo-text {
        color: var(--flashWhite);
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
        transition: .2s;
        cursor: pointer;
        height: max-content;
    }

    button:hover {
        background-color: var(--justBlue);
    }
</style>