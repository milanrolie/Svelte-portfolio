<script>

</script>
<div class="page-wrapper">
  <section class="projects-intro">
  <h3>The projects I have done</h3>
  <p>
    My projects are a mixture between real clients, personal and educational
    websites I've built.
  </p>
</section>

<section class="projects">
  <div class="text-wrapper" />
  <div class="projects-wrapper">
    <div class="project">
      <a target="_blank" href="https://milanrolie.github.io/proof-of-concept/">
      <p class="view-project">
        Ink One page - Ink One page - Ink One page - Ink One page - Ink One page
      </p>
      <img
      src="https://images.unsplash.com/photo-1562118506-b7271445f4e4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80"
      alt="test"
      />
    </a>
    </div>
    <div class="project">
      <p class="view-project orange">
        50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet
      </p>
      <img
        src="https://user-images.githubusercontent.com/112857190/214674458-0dcfa0fa-487c-4516-974d-c5165a603fca.png"
        alt="test"
      />
    </div>
    <div class="project">
      <a href="https://milanrolie.github.io/markk/" target="_blank">
      <p class="view-project orange">
        Markk - Markk - Markk - Markk - Markk - Markk - Markk - Markk
      </p>
      <img
        src="../src/assets/markk.png"
        alt="test"
      />
    </a>
    </div>

    <div class="project">
      <a href="https://tiny-pink-monkey-cuff.cyclic.app/" target="_blank">
      <p class="view-project orange">
        UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard - UltiTV Dashboard
      </p>
      <img
        src="src/assets/dashboard.jpg"
        alt="test"
      />
    </a>
    </div>
    <div class="project">
      <a href="https://ubicautrecht.nl/" target="_blank">
      <p class="view-project black">
        Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica
      </p>
      <img
      src="https://twintig-utrecht.nl/wp-content/uploads/2022/01/Ubica-NSlagmolen-29-september-202119-scaled.jpg"
      alt="test"
      />
    </a>
    </div>
    <div class="project">
      <a href="https://family-fitness.nl/" target="_blank">      <p class="view-project orange">
        Family Fitness - Family Fitness - Family Fitness - Family Fitness - Family Fitness - Family Fitness - Family Fitness 
      </p>
      <img
        src="https://images.unsplash.com/photo-1593476123561-9516f2097158?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80"
        alt="test"
      />
    </a>

    </div>
    <div class="project">
      <a target="_blank" href="https://precious-trench-coat-pig.cyclic.app/">
      <p class="view-project offset">
        visitekaartje - visitekaartje - visitekaartje - visitekaartje - visitekaartje
      </p>
      <img
        src="https://user-images.githubusercontent.com/112857190/218090470-43f74458-3437-4f0a-9d73-acdb72f2bb95.png"
        alt="test"
      />
    </a>
    </div>
    <div class="project">
      <a target="_blank" href="https://realtime-ultitv-production.up.railway.app/">
      <p class="view-project orange">
        Dashboard 2.0 - Dashboard 2.0 - Dashboard 2.0 - Dashboard 2.0 - Dashboard 2.0
      </p>
      <img
        src="https://user-images.githubusercontent.com/112857190/237328656-c2eaa029-4fc5-4b41-ac16-b211000562a3.png"
        alt="test"
      />
    </a>
    </div>
    <div class="project">
      <a href="https://milanrolie.com/" target="_blank">
        <div class="marquee">
      <p class="view-project">
        milanrolie.com - milanrolie.com - milanrolie.com - milanrolie.com - milanrolie.com
      </p>
      <img
        src="https://milanrolie.com/wp-content/uploads/2021/02/bier.png"
        alt="test"
      />
    </a>
    </div>
  </div>
</section>
</div>


<style>

  .projects-intro {
    margin-bottom: 5%;
    margin-left: 20%;
  }

  h3 {
    font-size: 3em;
    color: var(--dark);
    font-weight: 300;
  }

  p {
    font-size: 1.5em;
    font-weight: 200;
    max-width: 40%;
  }

  .projects {
    display: flex;
    flex-direction: row;
  }

  .text-wrapper {
    width: 20vw;
  }

  .projects-wrapper {
    display: flex;
    flex-direction: row;
    width: 80%;
    gap: 2vw;
    flex-wrap: wrap;
    margin-bottom: 10%;
  }

  .project {
    width: 30%;
    clip-path: inset(0 round 1em);
    position: relative;
    overflow: hidden;
  }

  

  .view-project {
    display: flex;
    position: absolute;
    align-items: center;
    font-size: 1.5em;
    z-index: 2;
    min-width: max-content;
    text-transform: uppercase;
    color: var(--webLavender);
    animation: projectMarquee 40s infinite linear;
    opacity: 0;
    height: 100%;
    width: max-content;
    transition: .2s;
    cursor: pointer;
    font-weight: 400;
    white-space: nowrap;
  }

  .orange {
    color: var(--bitterSweet);
  }

  .offset {
    margin-top: 10%;
  }

  .black {
    color: var(--dark);
  }

  @keyframes projectMarquee {

    0%  {
      transform: translateX(0%);
    }

    100%  {
      transform: translateX(-50%);
    }
  }


  img {
    aspect-ratio: 1;
    width: 100%;
    object-fit: cover;
    border-radius: 1em;
    transition: 0.3s;
    cursor: pointer;
    z-index: 1;
  }
/* 
  img:hover {
  }
  
  .view-project:hover {
    opacity: 1;
  }
   */
  .project:hover img {
    transform: scale(1.06);
  }
  
  .project:hover .view-project {

    opacity: 1;
  }

</style>
