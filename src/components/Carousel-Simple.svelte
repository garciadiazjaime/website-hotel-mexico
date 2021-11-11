<script>
  export let Carousel;
  export let slides;
  export let arrows = true

  const arrowsClase = arrows ? '' :'hide'
</script>

<style>
  .slide {
    position: relative;
  }
  .image-mask {
		background-color: black;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		opacity: 0.2;
	}
	.slide h4 {
		position: absolute;
		top: 38%;
		color: white;
		text-align: center;
		width: 100%;
		font-size: 15px;
		font-family: gotham;
	}
	.slide span {
		position: absolute;
		top: 48%;
		text-align: center;
		width: 100%;
		display: block;
		color: white;
		font-family: trento;
		font-size: 9px;
	}

  .arrow-control {
    width: 146px;
    height: 14px;
    position: absolute;
    bottom: -40px;
    z-index: 1;
  }

  .arrow-control:hover {
    cursor: pointer;
  }

  .arrow-control-prev {
    left: 0;
  }

  .arrow-control-next {
    right: 0;
  }

  img {
    display: block;
  }

  .hide {
    display: none;
  }

  @media (max-width: 480px) {
    .slide span {
      font-size: 6px;
    }
  }
</style>

<div class="carousel-container">
  <svelte:component
    this={Carousel}
    autoplay
    dots={false}
    autoplayDuration={7000}
    let:showPrevPage
    let:showNextPage
  >
    <div slot="prev" on:click={showPrevPage} class={`arrow-control arrow-control-prev ${arrowsClase}`}>
      <img src="/support/arrow-left.svg" alt="">
    </div>
    {#each slides as slide}
      <div class="slide">
        <img src={slide.path} alt={slide.id} id={slide.id} />
        <div class="image-mask"></div>
        {#if slide.name }
          <h4>CASA</h4>
          <span>{slide.name}</span>
        {/if}
      </div>
    {/each}
    <div slot="next" on:click={showNextPage} class={`arrow-control arrow-control-next ${arrowsClase}`}>
      <img src="/support/arrow-right.svg" alt="">
    </div>
  </svelte:component>
</div>

