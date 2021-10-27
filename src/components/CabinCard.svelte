<script>
  import { onMount } from 'svelte';
  export let cabinData = {};
  let Carousel;
  onMount(async () => {
    const module = await import('svelte-carousel');
    Carousel = module.default;
  });
</script>
<style>
  ul {
    columns: 2;
  }
  .col-container {
    display: flex;
    flex-direction: row;
  }
  a {
    display: block;
    color: white;
    background: darkolivegreen;
  }
</style>
<h3>{cabinData.name}</h3>
<svelte:component
  this={Carousel}
  autoplay
	autoplayDuration={5000}
>
  {#each cabinData.images as img}
    <img src={img.path} alt={img.id} id={img.id} />
  {/each}
</svelte:component>
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
  <a href="{cabinData.reservationUrl}" target="_blank">Reservar</a>
</div>

