<script>
  export let Carousel;
  export let cabinData;
</script>
<style>
  ul {
    columns: 2;
  }
  .col-container {
    display: flex;
    flex-direction: row;
    margin: 0 20px;
    align-content: flex-start;
    margin-bottom: 80px;
  }
  .col {
    flex-grow: 1;
    border-left: 1px solid goldenrod;
    padding-left: 20px;
  }
  .col:first-child {
    border-left: none;
    padding-left: none;
  }
  a {
    display: block;
    color: white;
    background: darkolivegreen;
    margin-left: 20px;
  }
  h3 {
    bottom: 30px;
    position: absolute;
    font-size: 48px;
    color:white;
    border-bottom: solid 1px white;
    padding-bottom: 20px;
    margin-left: 1em;
    text-transform: uppercase;
  }
  h3 span {
    font-size: 14px;
    display: block;
  }
  h4 {
    color: goldenrod;
    text-transform: uppercase;
    font-weight: normal;
  }
  .carousel-container {
    position: relative;
    margin-bottom: 25px;
  }
  ul {
    padding-left: 0;
    list-style: none;
  }
  li:before {
    content: "·";
    padding-right: 5px;
  }
  .arrow-control {
    background-color: goldenrod;
    width: 30px;
    height: 60px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 1;
  }
  .arrow-control:before {
    content: '';
    width: 15px;
    height: 15px;
    display: block;
    position: absolute;
    top: 50%;
    transform: rotate(45deg) translateY(-50%);;
  }

  .arrow-control-prev {
    left: 0;
  }
  .arrow-control-prev:before {
    border-bottom: 2px solid white;
    border-left: 2px solid white;
    left: 4px;
  }
  .arrow-control-next {
    right: 0;
  }
  .arrow-control-next:before {
    border-top: 2px solid white;
    border-right: 2px solid white;
    left: -2px;
  }
  .nav-dots {
    display: flex;
    flex-direction: row;
    position: absolute;
    bottom: 10px;
    column-gap: 10px;
  }
  .nav-dot {
    display: flex;
    width: 10px;
    height: 10px;
    background-color: white;
  }
  .active {
    background-color: goldenrod;
    cursor: pointer;
  }
  .action-button {
    text-decoration: none;
    padding: 10px 120px 10px 10px;
    position: relative;
  }
  .action-button:before {
    content: '';
    width: 60px;
    background-color: white;
    height: 1px;
    top: 50%;
    display: block;
    right: 20px;
    position: absolute;
  }
  .action-button:after {
    content: '';
    width: 7px;
    border-top: 1px solid white;
    border-right: 1px solid white;
    transform: rotate(45deg) translateY(-50%);
    height: 7px;
    top: 50%;
    display: block;
    right: 23px;
    position: absolute;
  }
</style>
<div class="carousel-container">
  <svelte:component
    this={Carousel}
    autoplay
    autoplayDuration={5000}
    let:showPrevPage
    let:showNextPage
    let:currentPageIndex
    let:pagesCount
    let:showPage
  >
    <div slot="prev" on:click={showPrevPage} class='arrow-control arrow-control-prev'></div>
    {#each cabinData.images as img}
      <img src={img.path} alt={img.id} id={img.id} />
    {/each}
      <div slot="next" on:click={showNextPage} class='arrow-control arrow-control-next'></div>
      <div slot="dots" class="nav-dots">
      {#each Array(pagesCount) as _, pageIndex (pageIndex)}
        <div class="nav-dot {currentPageIndex === pageIndex ? 'active' : ''}"
          on:click={() => showPage(pageIndex)}
        ></div>
      {/each}
    </div>
  </svelte:component>
  <h3><span>Casa</span>{cabinData.name}</h3>
  </div>
<div class="col-container">
  <div class="col">
    <h4>Capacidad</h4>
    <p>2 personas</p>
  </div>
  <div class="col">
    <h4>Características</h4>
    <ul>
      {#each cabinData.caracteristicas as caracteristica}
        <li>{caracteristica}</li>
      {/each}
    </ul>
  </div>
  <div class="col">
    <h4>Amenidades</h4>
    <ul>
      {#each cabinData.amenidades as amenidad}
        <li>{amenidad}</li>
      {/each}
    </ul>
  </div>
  <div>
    <a class="action-button" href="{cabinData.reservationUrl}" target="_blank">Reservar</a>
  </div>
</div>

