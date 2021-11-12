<script>
  export let Carousel;
  export let data;
</script>
<div class="container">
  <svelte:component
    this={Carousel}
    autoplay
    autoplayDuration={5000}
    let:showPrevPage
    let:showNextPage
  >
    <div slot="prev" on:click={showPrevPage} class='arrow-control arrow-control-prev'></div>
    {#each data as img}
      <img src={img} alt="" />
    {/each}
    <div slot="next" on:click={showNextPage} class='arrow-control arrow-control-next'></div>
    <div slot="dots" class="nav-dots"></div>
  </svelte:component>
  <div>
    <h3>Naturaleza</h3>
    <p>Paisajes que inspiran y nos llenan de orgullo; espacios naturales entre viñedos, vegetación endémica y encinares.</p>
    <img src="https://picsum.photos/40/40?random=16" alt="" />
  </div>
</div>
<style>
  .container {
    background: darkgreen;
    padding: 20px;
    position: relative;
    display: grid;
    grid-template-columns: 700px 1fr;
  }
  .arrow-control {
    width: 40px;
    height: 16px;
    position: absolute;
    bottom: 10px;
    z-index: 1;
  }
  .arrow-control:before {
    content: '';
    width: 7px;
    height: 7px;
    display: block;
    position: absolute;
    top: 50%;
    transform: rotate(45deg) translateY(-50%);
  }
  .arrow-control:after {
    content: '';
    width: 40px;
    height: 1px;
    display: block;
    position: absolute;
    top: 55%;
    background-color: white;

  }
  .arrow-control-prev {
    right: -100px;
  }
  .arrow-control-prev:before {
    border-bottom: 1px solid white;
    border-left: 1px solid white;
    left: -2px;
  }
  .arrow-control-next {
    right: -200px;
  }
  .arrow-control-next:before {
    border-top: 1px solid white;
    border-right: 1px solid white;
    right: 2px;
  }
</style>
