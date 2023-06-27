<script>

</script>
<div class="page-wrapper">
  <section class="projects-intro">
  <h3>The projects I have done</h3>
  <p>
    My projects are a mixture between real clients, personal and educational
    websites i've built.
  </p>
</section>

<section class="projects">
  <div class="text-wrapper" />
  <div class="projects-wrapper">
    <div class="project">
      <p class="view-project">
        50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet
      </p>
      <img
      src="https://images.unsplash.com/photo-1562118506-b7271445f4e4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80"
      alt="test"
      />
    </div>
    <div class="project">
      <p class="view-project">
        50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet
      </p>
      <img
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/05/urban-posters-free-mockup-psd-1072x0-c-default.jpg"
        alt="test"
      />
    </div>
    <div class="project">
      <p class="view-project orange">
        Markk - Markk - Markk - Markk - Markk - Markk - Markk - Markk
      </p>
      <img
        src="./src/assets/markk.png"
        alt="test"
      />
    </div>

    <div class="project">
      <img
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/05/urban-posters-free-mockup-psd-1072x0-c-default.jpg"
        alt="test"
      />
    </div>
    <div class="project">
      <img
        src="../src/assets/ubica.jpg"
        alt="test"
      />
    </div>
    <div class="project">
      <p class="view-project">
        Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica - Ubica
      </p>
      <img
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/06/iphone-14-pro-black-free-mockup-1072x0-c-default.jpg"
        alt="test"
      />
    </div>
    <div class="project">
      <p class="view-project">
        50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet
      </p>
      <img
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/06/iphone-14-pro-black-free-mockup-1072x0-c-default.jpg"
        alt="test"
      />
    </div>
    <div class="project">
      <p class="view-project">
        50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet
      </p>
      <img
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/06/iphone-14-pro-black-free-mockup-1072x0-c-default.jpg"
        alt="test"
      />
    </div>
    <div class="project">
      <p class="view-project">
        50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet - 50k for a better planet
      </p>
      <img
        src="https://www.mockupworld.co/wp-content/uploads/dynamic/2023/06/iphone-14-pro-black-free-mockup-1072x0-c-default.jpg"
        alt="test"
      />
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
    transition: .2s;
    cursor: pointer;
    font-weight: 400;
  }

  .orange {
    color: var(--bitterSweet);
  }

  @keyframes projectMarquee {

    0%  {
      transform: translateX(0%);
    }

    100%  {
      transform: translateX(-100%);
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
