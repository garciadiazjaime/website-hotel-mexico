<script>
  import Header from '../components/Header.svelte';
  import Nav from '../components/Nav.svelte';
  import { onMount } from 'svelte';

  let Carousel;
  onMount(async () => {
    const module = await import('svelte-carousel');
    Carousel = module.default;
  });

  const cabins = [
		{
			name: 'Sonora',
			image: 'https://picsum.photos/700/420?random=16',
		},
		{
			name: 'Sinaloa',
			image: 'https://picsum.photos/700/420?random=5',
		},
		{
			name: 'Chihuahua',
			image: 'https://picsum.photos/700/420?random=14',
		},
		{
			name: 'Durango',
			image: 'https://picsum.photos/700/420?random=13',
		},
		{
			name: 'Coahuila',
			image: 'https://picsum.photos/700/420?random=1',
		}
	];

</script>
<Header
  backgroundImage="https://picsum.photos/1000/620?random=1"
  bannerHeight="620"
>
 <span slot="subheader">
  <h3>Hotel México en la piel</h3>
  <a class="header-link" href="/reservaciones">Reserva</a>
 </span>
 <span slot="title">
  Un homenaje<br>a nuestro México
 </span>
 <div slot="icon" style="margin: 0 auto;">
  <img src="https://picsum.photos/100/100?random=15" alt="icon" />
</div>
</Header>
<Nav />
<div class="gray">
  <div class="small">
    <h3>Regresa<br>a casa</h3>
    <p>La calidez de nuestra tierra convertida en un espacio que te abraza, te da la bienvenida y parece que nunca se acaba.</p>
    <a href="/habitaciones">Ver habitaciones</a>
  </div>
  <div class="large">
    <svelte:component
    this={Carousel}
    autoplay
    autoplayDuration={5000}
    let:showPrevPage
    let:showNextPage
  >
    {#each cabins as cabin}
      <div class="cabin">
        <img src={cabin.image} alt="cabin.name" />
        <h3>
          Casa<br><span>{cabin.name}</span>
        </h3>
      </div>
    {/each}
    <div slot="dots" class="nav-dots"></div>
    <div slot="prev" on:click={showPrevPage} class='arrow-control arrow-control-prev'></div>
    <div slot="next" on:click={showNextPage} class='arrow-control arrow-control-next'></div>
  </svelte:component>
  </div>
  <div>
    <img src="https://picsum.photos/490/712?random=15" alt="icon" />
  </div>
  <div>
    <h3>El Hotel de México,<br>y el vino</h3>
    <p>Arquitectura que emerge de la tierra y se fusionan con su entorno, 13 “casas” que rinden homenaje a nuestro México, habitaciones con jacuzzi privado y una ubicación inigualable entre viñedos, áreas rocosas y un sorprendente bosque de encinos, distintas atmósferas dispuestas para emular de manera natural el territorio mexicano; una extensión de 15 hectáreas en donde espacios íntimos y de descanso convergen con espacios de celebración.</p>
    <p>Te invitamos a celebrar nuestra cultura<br>y disfrutar de nuestra tierra.</p>
    <a href="/reserva">Reserva ahora</a>
  </div>
</div>
<style>
  h3 {
    color: white;
    text-transform: uppercase;
    font-size: 20px;
  }
  .header-link {
    text-transform: uppercase;
    font-size: 14px;
    color: white;
    display: block;
    position: absolute;
    right: 0;
    top: 0;
    text-decoration: none;
  }

  .gray {
    background: lightgray;
  }
  .gray .small {
    flex-grow: 1;
  }
  .gray .large {
    position: relative;
  }
  .cabin {
    background: darkgreen;
    position: relative;
    padding-bottom: 28px;
    text-align: center;
    display: block;
  }
  .cabin h3 {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
    font-size: 14px;
  }
  .cabin img {
    width: 100%;
  }
  span {
    font-size: 40px;
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
    left: 15px;
  }
  .arrow-control-prev:before {
    border-bottom: 1px solid white;
    border-left: 1px solid white;
    left: -2px;
  }
  .arrow-control-next {
    right: 15px;
  }
  .arrow-control-next:before {
    border-top: 2px solid white;
    border-right: 2px solid white;
    right: 2px;
  }
</style>
