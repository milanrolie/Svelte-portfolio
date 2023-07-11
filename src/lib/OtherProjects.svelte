<script>
</script>

<section>
  <h3>Other projects</h3>
  <ul>
    <li>
      <div class="colored" />
      <p>Project over iets</p>
      <p class="date2">10-11-2019</p>
    </li>
    <li>
      <div class="colored" />
      <p>50k for a better planet</p>
      <p class="date2">10-11-2019</p>
    </li>
    <li>
      <div class="colored" />
      <p>Commentary tool</p>
      <p class="date2">10-11-2019</p>
    </li>
    <li>
      <div class="colored" />
      <p>Project over iets</p>
      <p class="date2">10-11-2019</p>
    </li>
    <li>
      <div class="colored" />
      <p>over iets Anders</p>
      <p class="date2">10-11-2019</p>
    </li>
    <li>
      <div class="colored" />
      <p>Ink Rio de Janeiro</p>
      <p class="date2">10-11-2019</p>
    </li>
  </ul>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    position: relative;
    width: 100%;
    /* background-color: rgb(193, 193, 255); */
    padding: 0;
    padding-top: 5%;
    margin-bottom: 4%;
  }

  h3 {
    position: absolute;
    top: 0;
    right: 0;
    color: var(--dark);
    font-size: 6vw;
    text-transform: none;
    line-height: 0.8em;
    font-weight: 700;
    text-transform: uppercase;
  }

  ul {
    /* width: 70%; */
  }

  li {
    display: flex;
    position: relative;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    text-decoration: none;
    list-style: none;
    font-size: 4vw;
    border-top: solid 2px;
    padding: 1px;
    padding: 5px 2%;
    transition:  0.3s;
  }

  p {
    color: var(--dark);
    transition: 0.3s;
  }

  li:hover p {
    color: var(--bitterSweet);
  }

  li:hover {
    cursor: pointer;
  }

  li:last-child {
    border-bottom: solid 2px;
  }

  ul .date2 {
    font-size: 0.5em;
  }

  .colored {
    position: absolute;
    top: 0;
    left: -100%;
    background-color: rgb(202, 202, 202);
    width: 100%;
    height: 100%;
    z-index: -1;
  }

  li:hover .colored {
    transition: cubic-bezier(1,0,.49,1.02) 1.2s;
    transform: translateX(100%);
  }


</style>
