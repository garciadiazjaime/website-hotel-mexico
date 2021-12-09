<script>
	import Content from '../components/Content.svelte'
	import Subheader from '../components/Subheader.svelte';
	import CabinCard from '../components/CabinCard.svelte';

	import { onMount } from 'svelte';

  let Carousel;
  onMount(async () => {
    const module = await import('svelte-carousel');
    Carousel = module.default;
  });

	const cabins = [
		{
			name: 'Baja California Sur',
			images: [
				{
				 path: '/habitaciones/01-Baja-California-Sur/01-MEXP_Baja-California-Sur-(1920x1080)_exterior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/02-MEXP_Baja-California-Sur-(1920x1080)_exterior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/03-MEXP_Baja-California-Sur-(1920x1080)_interior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/04-MEXP_Baja-California-Sur-(1920x1080)_interior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/05-MEXP_Baja-California-Sur-(1920x1080)_interior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/06-MEXP_Baja-California-Sur-(1920x1080)_interior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/07-MEXP_Baja-California-Sur-(1920x1080)_interior.jpg',
				 id: 'son1',
				},
				{
				 path: '/habitaciones/01-Baja-California-Sur/08-MEXP_Baja-California-Sur-(1920x1080)_interior.jpg',
				 id: 'son1',
				},
			],
			caracteristicas: [
				'Cama queen size',
				'Baño y regadera',
				'Sala con chimenea',
				'Barra comedor',
				'Patio terraza',
			],
			amenidades: [
				'Limpieza',
				'Refrigerador',
				'Televisión',
				'Internet (wi-fi)',
				'Aire (AC)',
			],
			reservationUrl: 'https://www.airbnb.com/users/200220394/listings',
		},
	];
</script>

<style>
	.main {
		margin-top: 40px;
		font-family: gotham;
		font-size: 18px;
	}
	.catalog {
		background-color: var(--color-hueso);
		margin: 0 auto;
		position: relative;
		margin-top: 100px;
		padding-top: 100px;
	}
	hr {
		border: none;
		margin: 0 auto 60px;
		position: relative;
		width: 1px;
		height: 1px;
		overflow: visible;
	}
	hr:before {
		content: '';
		display: block;
		position: absolute;
		left: 0;
		top: 0;
		width: 30px;
		height: 30px;
		border-color: var(--color-almendra);
		border-top: solid 1px var(--color-almendra);
		border-right: solid 1px var(--color-almendra);
		transform: rotate(-45deg);
	}
	hr:after {
		content: '';
		position: absolute;
		display: block;
		left: 0;
		top: -20px;
		width: 30px;
		height: 30px;
		background: none;
		margin: 0 auto;
		border-color: var(--color-almendra);
		border-bottom: solid 1px var(--color-almendra);
		border-left: solid 1px var(--color-almendra);
		transform: rotate(-45deg);
	}
	h1 {
		color: var(--color-almendra);
		text-align: center;
		margin: 60px 0 40px;
		font-family: mirage;
		font-weight: 200;
		font-size: 50px;
	}
	p {
		max-width: 570px;
		text-align: center;
		margin: 0 auto 80px;
		color: black;
	}
</style>
<div class="main">
	<Content>
		<Subheader color="var(--color-almendra)">Habitaciones</Subheader>
		<h1>Amar al Valle es amar a México</h1>
		<hr>
		<p>Cómodas habitaciones te darán la bienvenida, amenidades de lujo y un staff de primer nivel harán de tu estancia una experiencia inolvidable.</p>
	</Content>
	<div class="catalog">
		{#each cabins as cabin}
			<CabinCard cabinData={cabin} Carousel={Carousel} />
		{/each}
	</div>
</div>
