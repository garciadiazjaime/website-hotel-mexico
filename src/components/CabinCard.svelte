<script>
  import Share from './Share.svelte'

  export let Carousel;
  export let Lazy;
  export let cabinData;
</script>
<style>
  .content {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 100px;
		box-sizing: border-box;
	}
  ul {
    columns: 2;
  }
  .images {
    max-width: 1180px;
		max-height: 640px;
    margin: 0 auto;
  }
  .col-container {
    display: flex;
    flex-direction: row;
    align-content: flex-start;
    margin-bottom: 80px;
    font-size: 14px;
  }
  .col {
    flex-grow: 1;
  }
  .col:first-child {
    border-left: none;
    padding-left: none;
  }
  a {
    color: white;
    background: var(--color-verde);
    text-transform: uppercase;
    text-decoration: none;
    position: relative;
    width: 175px;
    height: 50px;
    display: flex;
    align-items: center;
    padding-left: 20px;
    font-size: 12px;
    box-sizing: border-box;
    margin-top: 10px;
  }
  a:after {
    content: '';
    width: 7px;
    border-top: 1px solid white;
    border-right: 1px solid white;
    transform: rotate(45deg) translateY(-50%);
    height: 7px;
    top: 46%;
    display: block;
    right: 23px;
    position: absolute;
  }
  .title {
    padding: 40px 0 20px;
    margin-bottom: 40px;
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid var(--color-almendra);
  }
  h3 {
    bottom: 30px;
    font-size: 10px;
    color:white;
    padding-bottom: 20px;
    text-transform: uppercase;
    color: var(--color-verde);
    font-family: trento;
  }
  span {
    font-size: 23px;
    display: block;
    font-family: gotham;
    margin-bottom: 6px;
  }
  h4 {
    color: var(--color-almendra);
    text-transform: uppercase;
    font-weight: normal;
  }
  .carousel-container {
    position: relative;
    margin-bottom: 25px;
  }
  @media (min-width: 960px) {
    .carousel-container {
      min-height: 640px;
    }
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
    background-color: var(--color-almendra);
    width: 45px;
    height: 120px;
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
  .arrow-control:hover {
    cursor: pointer;
  }
  .arrow-control-prev {
    left: 0;
  }
  .arrow-control-prev:before {
    border-bottom: 2px solid white;
    border-left: 2px solid white;
    left: 10px;
  }
  .arrow-control-next {
    right: 0;
  }
  .arrow-control-next:before {
    border-top: 2px solid white;
    border-right: 2px solid white;
    left: 4px;
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
    background-color: var(--color-almendra);
    cursor: pointer;
  }
  .social-media {
    position: relative;
  }  
  .clear {
    clear: both;
  }

  @media (max-width: 1080px) {
    .content {
      padding: 12px;
    }
    h3 {
      font-size: 3px;
    }
    .col-container {
      display: block;
    }
  }
</style>
<div class="carousel-container">
  <svelte:component this={Lazy} height={300}>
    <div class="images">
      <svelte:component
        this={Carousel}
        dots={false}
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
    </div>
  </svelte:component>
</div>

<div class="content">
  <div class="title">
    <div>
      <span>Casa</span>
      <h3>{cabinData.name}</h3>
    </div>
    <a href="{cabinData.reservationUrl}" target="_blank">Reserva</a>
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
    <div class="col social-media">
      <Share />
      <br class="clear">
    </div>
  </div>
</div>
