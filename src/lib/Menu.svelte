<script>

</script>

<nav>
    <div class="menu-wrapper">
        <p>studio</p>
    <ul>
        <li> <a href="">Projects</a> </li>
        <li> <a href="">Projects</a> </li>
        <li> <a href="">Projects</a> </li>
        <li> <a href="">Contact</a> </li>
    </ul>
</div>
</nav>

<style>

    nav {
        position: fixed;
        bottom: 2em;
        left: 50%;
        transform: translateX( -50%);
        z-index: 10;
     
    }
    
    .menu-wrapper {
        display: flex;
        flex-direction: row;
        background-color: rgba(0, 0, 0, 0.358);     
        padding: 1.5em 3em;
        border-radius: 1em;   
    }

    ul {
        display: flex;
        flex-direction: row;
        gap: 1em;
        background-color: rgba(0, 0, 0, 0.358);  
        height: 90%;   
    }

    li {
        list-style-type: none;
    }

    a {
        text-decoration: none;
        color: var(--gunMetal);
        font-family: inherit;
        text-transform: uppercase;
    }

</style>