<script>
    import arrow from '$lib/assets/arrow.svg';
</script> 
  



<div class="work-together">
    <div class="container">
        <button class="text">Work together</button>
        <!-- <img src={arrow} alt=""> -->
    </div>
</div>

<style>
    .work-together {
        position: fixed;
        right: 1em;
        top: 4em;
        height: max-content;
        width: 2em;
        background-color: var(--dark);
        z-index: 5;
        border-radius: 1em;
        transition: .2s;
    }

    .work-together:hover {
        background-color: var(--webLavender);
    }

    .work-together:hover .text {
        color: var(--dark);
    }

    .container {
        position: relative;
        display: flex;
        flex-direction: column;
        gap: 1em;
        align-items: center;
        justify-content: space-between;
        padding: 1em;
        height: max-content;
        overflow: hidden;

    }

    .text {
        writing-mode: vertical-lr;
        width: max-content;
        color: var(--gunMetal);
        text-transform: uppercase;
        font-size: .9em;
        background-color: rgba(255, 255, 255, 0);
        border: none;
        cursor: pointer;
        padding: 0 1em ;
    }

    img {
        transform: scale(.8);
    }
</style>